<script lang="ts">
    import Header from './components/Header.svelte'
    import Footer from './components/Footer.svelte'

    import Home from './components/Home.svelte'
    import {onMount} from "svelte";
    import About from "./components/About.svelte";
    import Skills from "./components/Skills.svelte";
    import Portfolio from "./components/Portfolio.svelte";
    import Contact from "./components/Contact.svelte";

    const scroll = () => {
        const sections = document.querySelectorAll('section');
        const links = document.querySelectorAll('nav a');

    }

    onMount(() => {
        let dark = localStorage.getItem('theme') === 'dark'
        let body = document.body
        body.classList.toggle('dark', dark);
    });
</script>

<Header />
<main>
    <Home/>
    <About/>
    <Skills/>
    <Portfolio/>
    <Contact/>
</main>
