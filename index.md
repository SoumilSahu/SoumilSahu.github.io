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
    }

    .foreground-text {
        position: absolute;
        top: 45%;
        left: 25%;
        transform: translateY(-50%);
        font-size: 4rem;
        font-weight: bold;
        line-height: 1.1;
        color: #ffffff;
        text-shadow: 3px 3px 10px rgba(0, 0, 0, 0.9);
        pointer-events: none; /* Lets you click things behind the text if needed */
    }

    .foreground-text span {
        color: var(--accent);
    }

    /* Scroll Indicator */
    .scroll-down {
        position: absolute;
        bottom: 30px;
        left: 50%;
        transform: translateX(-50%);
        font-size: 2rem;
        color: var(--accent);
        animation: bob 2s infinite ease-in-out;
    }

    @keyframes bob {
        0%, 100% { transform: translate(-50%, 0); }
        50% { transform: translate(-50%, -15px); }
    }

    /* Summary Section */
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
    <div class="hero-right"></div>
    <div class="foreground-text">
        You have spiralled into<br>
        <span>Soumil Sahu's</span><br>
        webpage.
    </div>
    <div class="scroll-down">↓</div>
</div>

<div class="summary-box">
    <h2>About Me</h2>
    <p>I am a researcher studying the extremes of the universe. My work primarily focuses on the equation of state of dense matter in neutron stars and continuous gravitational wave emissions.</p>
    <p>Use the navigation bar above to explore my research, read my blog, or check out what life is like at IUCAA.</p>
</div>
