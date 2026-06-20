---
layout: default
title: Contact
---

<style>
    .contact-container {
        max-width: 600px;
        margin: 2rem auto;
        background: var(--bg-mid);
        padding: 2.5rem;
        border-radius: 8px;
        box-shadow: 0 10px 30px rgba(0,0,0,0.5);
    }
    
    .form-group {
        margin-bottom: 1.5rem;
        display: flex;
        flex-direction: column;
    }

    .form-group label {
        margin-bottom: 0.5rem;
        color: var(--accent);
        font-weight: 500;
        letter-spacing: 1px;
    }

    .contact-container input,
    .contact-container textarea {
        background: var(--bg-deep);
        border: 1px solid var(--bg-light);
        color: var(--text-main);
        padding: 1rem;
        border-radius: 4px;
        font-family: inherit;
        font-size: 1rem;
        transition: border-color 0.3s ease;
    }

    .contact-container input:focus,
    .contact-container textarea:focus {
        outline: none;
        border-color: var(--accent);
    }

    .submit-btn {
        background: transparent;
        color: var(--accent);
        border: 2px solid var(--accent);
        padding: 1rem 2rem;
        font-size: 1.1rem;
        font-weight: bold;
        cursor: pointer;
        border-radius: 4px;
        transition: all 0.3s ease;
        width: 100%;
        margin-top: 1rem;
    }

    .submit-btn:hover {
        background: var(--accent);
        color: var(--bg-deep);
    }
</style>

# Get in Touch

Send me a nudge! Whether you want to discuss the depths of the universe or simply wanna say hello, drop a message below.

<div class="contact-container">
    <form action="https://formspree.io/f/mvzneebo" method="POST">
        
        <div class="form-group">
            <label for="name">Name</label>
            <input type="text" id="name" name="name" required>
        </div>
        
        <div class="form-group">
            <label for="email">Email</label>
            <input type="email" id="email" name="_replyto" required>
        </div>
        
        <div class="form-group">
            <label for="message">Message</label>
            <textarea id="message" name="message" rows="6" required></textarea>
        </div>
        
        <input type="hidden" name="_subject" value="New message from your portfolio!">
        
        <button type="submit" class="submit-btn">Nudge Soumil!</button>
    </form>
</div>
