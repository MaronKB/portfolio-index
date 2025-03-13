<script lang="ts">
import {FontAwesomeIcon} from "@fortawesome/svelte-fontawesome";
import {faHashtag, faHome, faTimes, faUpRightFromSquare} from "@fortawesome/free-solid-svg-icons";
import {faGithub} from "@fortawesome/free-brands-svg-icons";

export let opened: boolean = false;
export let title: string = "Modal";
export let link: string = "";
export let img: string = "";
export let source: string = "";
export let tags: string[] = [];

</script>

<div class="modal-background" class:opened={opened}>
    <div class="modal">
        <header class="header">
            <div class="title">
                <h3>{title}</h3>
                <a href={link} target="_blank">{link}</a>
            </div>
            <div class="links">
                <a href={link} target="_blank"><FontAwesomeIcon icon={faHome}/></a>
                <a href={source}><FontAwesomeIcon icon={faGithub}/></a>
            </div>
            <button type="button" class="close" onclick={() => opened = false}>
                <span><FontAwesomeIcon icon={faTimes}/></span>
            </button>
        </header>
        <img src={img} alt="img" class="image"/>
        <div class="content">
            <div class="tags">
                {#each tags as tag}
                    <span><FontAwesomeIcon icon={faHashtag}/>{tag}</span>
                {/each}
            </div>
            <div class="item">
                <h3>Overview</h3>
                <slot name="overview"></slot>
            </div>
            <div class="item">
                <h3>Tech Stack</h3>
                <slot name="tech-stack"></slot>
            </div>
            <div class="item">
                <h3>Key Features</h3>
                <slot name="key-features"></slot>
            </div>
            <div class="item">
                <h3>Role</h3>
                <slot name="role"></slot>
            </div>
            <div class="item">
                <h3>Development Period</h3>
                <slot name="development-period"></slot>
            </div>
            <div class="item">
                <h3>Outcome</h3>
                <slot name="outcome"></slot>
            </div>
            <div class="item">
                <h3>Challenges</h3>
                <slot name="challenges"></slot>
            </div>
            <a class="source" href={source}><FontAwesomeIcon icon={faGithub}/>Source<FontAwesomeIcon icon={faUpRightFromSquare}/></a>
        </div>
    </div>
</div>

<style>
    .modal-background {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        background: rgba(0, 0, 0, 0.5);
        z-index: 100;
        opacity: 0;
        pointer-events: none;
        transition: opacity 0.3s;
    }
    .modal-background.opened {
        opacity: 1;
        pointer-events: auto;
    }

    .modal {
        width: 80%;
        max-width: 600px;
        height: 80%;
        max-height: 800px;
        display: flex;
        flex-direction: column;
        background: var(--background-color-2);
        border-radius: 5px;
        box-shadow: 0 0 1rem rgba(0, 0, 0, 0.1);
        overflow: hidden;
    }

    .header {
        flex: none;
        width: 100%;
        height: 60px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom: 1px solid var(--border-color);
    }

    .title {
        flex: 1;
        padding: 0 20px;
    }
    .title > h3 {
        font-size: 18px;
    }
    .title > a {
        font-size: 12px;
        color: var(--text-color-3);
        opacity: 0.75;
    }

    .links {
        display: flex;
    }
    .links > a {
        width: 60px;
        height: 60px;
        font-size: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        background: none;
        border: none;
        cursor: pointer;
    }
    .links > a:hover {
        background: var(--background-color-3);
    }

    .header button {
        width: 60px;
        height: 60px;
        font-size: 24px;
        background: none;
        border: none;
        cursor: pointer;
    }

    .header button:hover {
        background: var(--background-color-3);
    }

    .image {
        flex: none;
        width: 100%;
        height: 160px;
        background: white;
        object-fit: cover;
    }

    .content {
        flex: 1;
        width: 100%;
        padding: 20px 30px;
        overflow-y: auto;
    }

    .tags {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
        align-items: center;
        gap: 4px;
        font-size: 13px;
    }
    .tags span {
        display: inline-flex;
        justify-content: center;
        align-items: center;
        gap: 2px;
        white-space: nowrap;
        color: var(--text-color-3);
        padding: 3px 8px;
        border: 1px solid var(--text-color-3);
        border-radius: 2px;
    }

    .item {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        padding: 10px 0;
    }
    .item h3 {
        width: 100%;
        font-size: 16px;
        color: var(--text-color-3);
        padding: 0 0 5px 0;
        border-bottom: 1px solid var(--text-color-3);
        margin: 0 0 10px 0;
        opacity: 0.75;
    }

    .source {
        width: 100%;
        height: 40px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        gap: 5px;
        font-size: 14px;
        color: var(--text-color-3);
        opacity: 0.75;
        margin: 20px 0 0 0;
    }
</style>