<script>

import {FontAwesomeIcon} from "@fortawesome/svelte-fontawesome";
import {faEnvelope} from "@fortawesome/free-solid-svg-icons";
import {faGithub, faInstagram, faXTwitter} from "@fortawesome/free-brands-svg-icons";
</script>

<section id="contact">
    <h2>Contact</h2>
    <div class="container">
        <a href="mailto:asdfgh7913@gmail.com" target="_blank" class="contact">
            <div class="icon email">
                <FontAwesomeIcon icon={faEnvelope}/>
                <h3>Email</h3>
            </div>
        </a>
        <a href="https://x.com/asdfgh7913" target="_blank" class="contact">
            <div class="icon twitter">
                <FontAwesomeIcon icon={faXTwitter}/>
                <h3>X-Twitter</h3>
            </div>
        </a>
        <a href="https://github.com/MaronKB" target="_blank" class="contact">
            <div class="icon github">
                <FontAwesomeIcon icon={faGithub}/>
                <h3>GitHub</h3>
            </div>
        </a>
        <a href="https://www.instagram.com/heehee_iron/" target="_blank" class="contact">
            <div class="icon instagram">
                <FontAwesomeIcon icon={faInstagram}/>
                <h3>Instagram</h3>
            </div>
        </a>
    </div>
</section>

<style>
    .container {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: repeat(2, 1fr);
        transform: rotate(-45deg);
        gap: 5px;
        margin: 0 0 80px 0;
    }

    .contact {
        width: 140px;
        height: 140px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        background: var(--background-color-3);
        border-radius: 10px;
    }
    .contact:hover {
        background: var(--background-color);
    }

    .icon {
        position: relative;
        width: 60px;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 32px;
        background: var(--background-color);
        border-radius: 50%;
        transform: rotate(45deg);
    }
    .email {
        color: black;
        background: white;
    }
    .twitter {
        color: white;
        background: black;
    }
    .github {
        color: white;
        background: black;
    }
    .instagram {
        color: white;
        background: radial-gradient(circle at 30% 107%,#fdf497 0,#fdf497 5%,#fd5949 45%,#d6249f 60%,#285aeb 90%);
    }

    .icon h3 {
        position: absolute;
        bottom: -10px;
        height: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: var(--font-heading), sans-serif;
        font-size: 12px;
        font-weight: normal;
        text-transform: uppercase;
        white-space: nowrap;
        color: var(--background-color-2);
        background: var(--text-color-3);
        padding: 0 15px;
        margin: 0;
    }
    @media print {
        section {
            display: none;
        }
    }
</style>