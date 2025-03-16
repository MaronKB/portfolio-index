<footer>
    <p>© 2025 MRKB Portfolio</p>
    <p>Powered by SvelteKit</p>
    <p>Developed by <a href="/">MRKB</a></p>
</footer>

<style>
    footer {
        height: 40px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        gap: 10px;
        background: var(--background-color-3);
        padding: 0 20px;
    }

    footer p {
        font-size: 12px;
    }

    footer a {
        color: var(--text-highlight);
        text-decoration: none;
    }

    footer a:hover {
        text-decoration: underline;
    }
</style>