---
layout: default
title: Home
---

<style>
    /* Hero Screen */
    .hero {
        display: flex;
        height: calc(100vh - 70px);
        width: 100vw;
        position: relative;
    }

    .hero-left {
        width: 40%;
        /* background-image: url('/assets/profile.jpg'); */
        background-image: url('https://github.com/soumilsahu.png');
        background-size: cover;
        background-position: center;
        border-right: 2px solid var(--accent);
    }

    .hero-right {
        width: 60%;
        background: radial-gradient(circle at top right, var(--bg-mid), var(--bg-deep));
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 3rem; /* Add generous padding to prevent content touching edges */
    }

    /* Style for the main hero text */
    .hero-right h1 {
        font-size: 3rem; /* Slightly reduced size for better fit, adjust as needed */
        font-weight: bold;
        line-height: 1.2;
        color: #ffffff;
        text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.9);
        margin-bottom: 1rem; /* Space below the heading */
        pointer-events: none; /* Let clicks pass through if needed, though less critical now */
    }

    .hero-right h1 span {
        color: var(--accent);
    }

    /* Scroll Indicator - repositioned to be centered within hero-right */
    .scroll-down {
        font-size: 2.5rem;
        color: var(--accent);
        animation: bob 2s infinite ease-in-out;
        margin-top: 2rem; /* Add separation from the main text */
    }

    @keyframes bob {
        0%, 100% { transform: translateY(0); }
        50% { transform: translateY(-15px); }
    }

    /* Summary Section - unchanged */
    .summary-box {
        max-width: 800px;
        margin: 100px auto;
        padding: 40px;
        background-color: var(--bg-mid);
        border-radius: 8px;
        box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        text-align: center;
        font-size: 1.2rem;
    }
</style>

<div class="hero">
    <div class="hero-left"></div>
    <div class="hero-right">
        <h1>You have inspiralled into<br>
        <span>Soumil Sahu's</span><br>
        webpage.</h1>
        <div class="scroll-down">↓</div>
    </div>
</div>

<div class="summary-box" id="about-container">
    <h2>About Me</h2>
    <p class="type-text" data-text="I am a PhD research scholar, a baby in this hierarchy of research, trying to explore the extremes of the universe. My work primarily focuses on the multimessenger astrophysical study of Neutron Stars."></p>
    <p class="type-text" style="font-style: italic;" data-text="I am nothing but a part of nature trying to understand itself."></p>
    <p class="type-text" data-text="Use the navigation bar above to explore my research, read my blog, or check out what life is like at IUCAA."></p>
</div>

<style>
    /* Optional: Adds a blinking cursor to the end of the text being typed */
    .type-text::after {
        content: '|';
        color: var(--accent);
        animation: blink 1s step-end infinite;
        opacity: 0; /* Hidden by default */
    }
    .type-text.is-typing::after {
        opacity: 1; /* Visible only while typing */
    }
    @keyframes blink {
        50% { opacity: 0; }
    }
</style>

<script>
    // Set up the tripwire
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            // When the summary box enters the screen
            if (entry.isIntersecting) {
                const paragraphs = entry.target.querySelectorAll('.type-text');
                let totalDelay = 0; // Tracks the time delay for each letter

                paragraphs.forEach((p) => {
                    // Prevent it from re-typing if the user scrolls up and down
                    if (p.innerHTML !== "") return; 
                    
                    const text = p.getAttribute('data-text');
                    p.classList.add('is-typing'); // Turn on the blinking cursor
                    
                    // Loop through every letter in the paragraph
                    for (let i = 0; i < text.length; i++) {
                        setTimeout(() => {
                            // Add the letter to the screen
                            p.innerHTML += text.charAt(i);
                            
                            // Turn off the cursor when the very last letter is typed
                            if (i === text.length - 1) {
                                p.classList.remove('is-typing');
                            }
                        }, totalDelay);
                        
                        // Typing speed: 30 milliseconds per letter
                        totalDelay += 30; 
                    }
                    
                    // Add a brief pause between paragraphs
                    totalDelay += 500; 
                });
            }
        });
    }, { threshold: 0.5 }); // Triggers when 50% of the box is visible on screen

    // Attach the tripwire to the summary box
    observer.observe(document.getElementById('about-container'));
</script>
