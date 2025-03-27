<script lang="ts">

    import {onMount} from "svelte";
    import Logo from '/src/assets/logo.svg?raw';
    import Title from '/src/assets/title.svg?raw';

    const sleep = async (ms: number) => {
        return new Promise(resolve => setTimeout(resolve, ms));
    }

    let bg: HTMLDivElement;

    const jobArr = [
        'Frontend_Developer',
        'Backend_Developer',
        'Fullstack_Developer',
        'Web_Developer',
        'Web_Publisher',
        'Web_Designer',
        'UI/UX_Designer'
    ]

    const createBackground = async () => {
        let text = "";
        for (let i = 0; i < 100; i++) {
            jobArr.forEach(job => {
                text += `<span class="bg-text" style="opacity: 0.15; transition: all 0.3s">${job}</span><span style="opacity: 0.15">&</span>`;
            });
        }
        bg.innerHTML = text;
    }

    let subtitle: HTMLSpanElement;

    const rewriteSubtitle = async () => {
        const remove = async () => {
            while (subtitle.innerHTML.length > 0) {
                subtitle.innerHTML = subtitle.innerHTML.slice(0, -1);
                await sleep(50);
            }
        }

        const lightsOut = async () => {
            const spans = Array.from(bg.children).filter((element: Element) => element.className === 'bg-text') as HTMLSpanElement[];
            spans.forEach((element: HTMLSpanElement) => {
                element.style.opacity = '0.15';
            });
        }

        const write = async (text: string) => {
            for (let i = 0; i < text.length; i++) {
                subtitle.innerHTML += text[i];
                await sleep(50);
            }
        }

        const lightsOn = async (text: string) => {
            const spans = Array.from(bg.children).filter((element: Element) => element.innerHTML === text) as HTMLSpanElement[];
            spans.forEach((element: HTMLSpanElement) => {
                element.style.opacity = '0.75';
            });
        }

        while (true) {
            for (let i = 0; i < jobArr.length; i++) {
                await lightsOut();
                await remove();
                await sleep(100);
                await lightsOn(jobArr[i]);
                await write(jobArr[i]);
                await sleep(1000);
            }
        }
    }

    onMount(async () => {
        createBackground();
        //rewriteSubtitle();
    });
</script>

<section id="home">
    <div class="logo">{@html Logo}</div>
    <h1 class="title">{@html Title}</h1>
    <h2 class="subtitle"><span class="prefix">AS_A_</span><span class="text" bind:this={subtitle}></span></h2>
    <div class="bg" bind:this={bg}></div>
</section>

<style>
    section {
        position: relative;
        height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 20px;
        color: var(--text-color);
        background: linear-gradient(135deg, var(--background-color) 50%, var(--background-color-2) 50%);
        perspective: 1000px;
        overflow: hidden;
    }
    .logo {
        flex: none;
        width: 50%;
        min-width: 200px;
        max-width: 300px;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 40px;
        border-radius: 50%;
        margin: 100px 0 0 0;
        fill: var(--text-color);
        object-fit: contain;
    }
    @media (max-width: 768px) {
        .logo {
            padding: 20px;
        }
    }
    @media (max-width: 480px) {
        .logo {
            padding: 0;
        }
    }
    .title {
        width: 300px;
        height: 80px;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 10px;
        fill: var(--text-color);
    }
    .subtitle {
        width: 100%;
        height: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: var(--font-text), sans-serif;
        font-size: 18px;
        text-align: center;
        text-transform: uppercase;
        letter-spacing: 2px;
        line-height: 100%;
    }
    .subtitle::after {
        display: inline-block;
        content: '';
        align-self: flex-end;
        width: 10px;
        height: 4px;
        background-color: var(--text-color-3);
        margin: 0 0 0 5px;
        opacity: 0.75;
        animation: blink 0.5s infinite;
    }
    .prefix {
        color: var(--text-color-3);
        opacity: 0.75;
    }
    .text {
        color: var(--text-color);
    }
    .bg {
        position: absolute;
        width: 2500px;
        height: 100%;
        font-family: var(--font-heading), sans-serif;
        font-weight: var(--font-weight-light);
        font-size: 80px;
        text-align: justify-all;
        text-transform: uppercase;
        letter-spacing: 2px;
        line-height: 100%;
        white-space: wrap;
        word-break: break-all;
        padding: 0 0 0 20px;
        transform: rotateX(20deg) rotateY(10deg) rotateZ(-20deg) translateZ(200px);
        pointer-events: none;
        overflow: hidden;
    }
    @keyframes blink {
        0%, 100% {
            opacity: 1;
        }
        50% {
            opacity: 0;
        }
    }
    @media (max-width: 768px) {
        .title {
            width: 300px;
        }
        .bg {
            font-size: 60px;
            padding: 0 0 0 15px;
        }
        .bg::after {
            width: 30px;
            height: 15px;
            margin: 0 0 0 3px;
        }
    }
    @media (max-width: 480px) {
        .title {
            width: 200px;
        }
        .bg {
            font-size: 40px;
            padding: 0 0 0 10px;
        }
        .bg::after {
            width: 20px;
            height: 10px;
            margin: 0 0 0 2px;
        }
    }
    @media print {
        .subtitle {
            display: none;
        }
    }
</style>
