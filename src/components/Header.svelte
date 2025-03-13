<script lang="ts">
    import Logo from '/src/assets/logo.svg?raw'
    import LogoWithText from '/src/assets/logo-text.svg?raw'
    import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome'
    import {
        faBriefcase,
        faChalkboardUser,
        faHome, faIdCard,
        faMoon,
        faScrewdriverWrench,
        faSun,
    } from '@fortawesome/free-solid-svg-icons'
    import { faTwitter, faInstagram, faGithub } from '@fortawesome/free-brands-svg-icons'
    import {onMount} from "svelte";

    let theme: HTMLInputElement;
    let dark = localStorage.getItem('theme') === 'dark';

    const setTheme = () => {
        dark = theme.checked;
        localStorage.setItem('theme', theme.checked ? 'dark' : 'light');
        document.body.classList.toggle('dark', theme.checked);
    }

    let folded = localStorage.getItem('folded') === 'true';
    const fold = () => {
        folded = !folded;
        localStorage.setItem('folded', folded.toString());
    }

    const scroll = (ev: Event) => {
        ev.preventDefault();

        const sections = document.querySelectorAll('section');
        const target = ev.target as HTMLAnchorElement;
        const targetSection = document.querySelector(`#${target.dataset.target}`) as HTMLElement;
        if (targetSection) {
            const main = document.querySelector('main') as HTMLElement;
            main.scrollTo({
                top: targetSection.offsetTop,
                behavior: 'smooth'
            });
        }
    }

    let isScreen = window.innerWidth < 768;
    onMount(() => {
        const listener = () => {
            if (window.innerWidth < 768) {
                isScreen = true;
                folded = true;
            } else {
                isScreen = false;
                folded = localStorage.getItem('folded') === 'true';
            }
        }
        window.addEventListener('resize', listener);
        return () => {
            window.removeEventListener('resize', listener);
        }
    });
</script>

<header class="header {folded && 'folded'}">
    <div class="img">
    {#if folded}
        {@html Logo}
    {:else}
        {@html LogoWithText}
    {/if}
    </div>
    <nav class="nav">
        <button data-target="home" class="link" class:active={false} on:click={scroll}>
            {#if folded}
                <FontAwesomeIcon icon={faHome}/>
                <div class="tooltip">Home</div>
            {:else}
                Home
            {/if}
            <span class="marker"></span>
        </button>
        <button data-target="about" class="link" class:active={false} on:click={scroll}>
            {#if folded}
                <FontAwesomeIcon icon={faChalkboardUser}/>
                <div class="tooltip">About</div>
            {:else}
                About
            {/if}
            <span class="marker"></span>
        </button>
        <button data-target="skills" class="link" class:active={false} on:click={scroll}>
            {#if folded}
                <FontAwesomeIcon icon={faScrewdriverWrench}/>
                <div class="tooltip">Skills</div>
            {:else}
                Skills
            {/if}
            <span class="marker"></span>
        </button>
        <button data-target="portfolio" class="link" class:active={false} on:click={scroll}>
            {#if folded}
                <FontAwesomeIcon icon={faBriefcase}/>
                <div class="tooltip">Portfolio</div>
            {:else}
                Portfolio
            {/if}
            <span class="marker"></span>
        </button>
        <button data-target="contact" class="link" class:active={false} on:click={scroll}>
            {#if folded}
                <FontAwesomeIcon icon={faIdCard}/>
                <div class="tooltip">Contact</div>
            {:else}
                Contact
            {/if}
            <span class="marker"></span>
        </button>
    </nav>
    <div class="theme">
        <input type="checkbox" id="theme" bind:this={theme} on:change={setTheme} checked={dark}/>
        <label for="theme">
            <span class="toggle"></span>
            {#if dark}
                <span class="icon"><FontAwesomeIcon icon={faMoon} style="width: 100%; height: 100%"/></span>
            {:else}
                <span class="icon"><FontAwesomeIcon icon={faSun} style="width: 100%; height: 100%"/></span>
            {/if}
        </label>
    </div>
    <div class="socials">
        <a href="/" class="social"><FontAwesomeIcon icon={faTwitter}/></a>
        <a href="/" class="social"><FontAwesomeIcon icon={faGithub}/></a>
        <a href="/" class="social"><FontAwesomeIcon icon={faInstagram}/></a>
    </div>
    {#if !folded}
        <div class="copy">
            <p>&copy; 2021 MRKB</p>
        </div>
    {/if}
    {#if !isScreen}
        <button class="opener" aria-label="expand/fold" on:click={fold}><span class="open"></span></button>
    {/if}
</header>

<style>
    .header {
        position: relative;
        width: 160px;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        background: linear-gradient(135deg, var(--background-color), var(--background-color-3));
        transition: width 0.3s;
        z-index: 100;
    }
    .header.folded {
        width: 60px;
    }

    .img {
        width: 100%;
        height: auto;
        padding: 40px 30px;
        fill: var(--text-color);
        object-fit: contain;
        transition: padding 0.3s;
    }
    .header.folded .img {
        padding: 30px 10px;
    }

    .nav {
        width: 100%;
        display: flex;
        flex-direction: column;
        margin: auto 0;
    }
    .link {
        position: relative;
        width: 100%;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 16px;
        text-transform: uppercase;
        text-decoration: none;
        letter-spacing: 5px;
        color: var(--text-color);
        background-color: transparent;
        border-bottom: 1px solid var(--background-color-3);
        transition: background-color 0.3s;
    }
    .link:last-child {
        border-bottom: none;
    }
    .link:hover {
        background-color: var(--background-color-2);
    }
    .link .tooltip {
        position: absolute;
        top: 50%;
        left: 100%;
        transform: translate(10px, -50%);
        height: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 12px;
        color: var(--text-color);
        background-color: var(--background-color-2);
        padding: 0 20px;
        border-radius: 5px;
        opacity: 0;
        pointer-events: none;
        transition: opacity 0.3s;
    }
    .link:hover .tooltip {
        opacity: 1;
    }
    .link .marker {
        position: absolute;
        top: 50%;
        left: 100%;
        width: 10px;
        height: 10px;
        background-color: var(--text-color);
        border-radius: 2px;
        transform: translate(10px, -50%) rotate(45deg);
        opacity: 0;
        transition: opacity 0.3s;
    }
    .link.active .marker {
        opacity: 1;
    }

    .theme {
        flex: none;
        width: 100%;
        height: fit-content;
        display: flex;
        justify-content: center;
        align-items: flex-end;
        gap: 5px;
        background: linear-gradient(180deg, transparent, var(--background-color-2));
        padding: 10px 0;
    }
    .header.folded .theme {
        padding: 10px 0;
    }
    .theme input {
        display: none;
    }
    .theme label {
        position: relative;
        width: 40px;
        height: 40px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: var(--background-color);
        border-radius: 50%;
        cursor: pointer;
        transition: transform 0.3s;
    }
    .header.folded .theme label {
        transform: rotate(90deg);
    }
    .icon {
        position: absolute;
        top: 3px;
        left: 3px;
        width: calc(100% - 6px);
        height: calc(100% - 6px);
        display: flex;
        justify-content: center;
        align-items: center;
        color: var(--text-color);
        background-color: var(--background-color-2);
        padding: 7px;
        border-radius: 50%;
    }
    .header.folded .icon {
        transform: rotate(-90deg);
    }
    .toggle {
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        color: var(--background-color);
        background: linear-gradient(135deg, var(--text-color) 50%, transparent 50%);
        padding: 10px;
        border-radius: 50%;
        transition: transform 0.3s;
    }
    .theme input:checked + label .toggle {
        transform: rotate(180deg);
    }

    .socials {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 10px;
        background-color: var(--background-color-2);
        padding: 10px 20px;
        transition: padding 0.3s;
    }
    .header.folded .socials {
        flex-direction: column;
        padding: 0 0 20px 0;
    }
    .social {
        width: 30px;
        height: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 20px;
        color: var(--text-color);
        border-radius: 50%;
    }

    .copy {
        width: 100%;
        height: 40px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 12px;
        color: var(--text-color);
        background-color: var(--background-color-2);
    }

    .opener {
        position: absolute;
        top: 50%;
        left: 100%;
        transform: translate(-50%, -50%) rotate(45deg);
        width: 20px;
        height: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: var(--background-color-3);
        border-radius: 0 5px;
        z-index: 100;
    }
    .open {
        width: 14px;
        height: 14px;
        background: linear-gradient(45deg, var(--text-color) 45%, transparent 45% 55%, var(--text-color) 55%);
        opacity: 0.4;
    }
    .opener:hover .open {
        opacity: 1;
    }
</style>