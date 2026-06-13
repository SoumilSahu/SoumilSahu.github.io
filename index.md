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
        background-image: url('/assets/profile.jpg');
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

<div class="summary-box">
    <h2>About Me</h2>
    <p>I am a researcher studying the extremes of the universe. My work primarily focuses on the equation of state of dense matter in neutron stars and continuous gravitational wave emissions.</p>
    <p>Use the navigation bar above to explore my research, read my blog, or check out what life is like at IUCAA.</p>
</div>
