<script lang="ts">
    import Modal from "./Modal.svelte";
    import {faHashtag} from "@fortawesome/free-solid-svg-icons";
    import {FontAwesomeIcon} from "@fortawesome/svelte-fontawesome";

    export let title: string;
    export let image: string;
    export let address: string;
    export let link: string;
    export let source: string;
    export let tags: string[];
    export let summary: string;

    let opened = false;
</script>

<div class="link">
    <button type="button" class="image" onclick={() => window.open(link)}>
        <img src={image} alt={title}/>
    </button>
    <div class="text">
        <h4>{title}</h4>
        <a href={link} target="_blank">{address}</a>
        <hr/>
        <div class="tags">
            {#each tags as tag}
                <span><FontAwesomeIcon icon={faHashtag}/>{tag}</span>
            {/each}
        </div>
        <div class="summary">
            <p>{summary}</p>
        </div>
    </div>
    <button type="button" class="expand" onclick={() => opened = !opened}>
        <span>상세</span>
    </button>
</div>
<Modal opened={opened} title={title} link={link} img={image} source={source} tags={tags}>
    <p slot="overview">{summary}</p>
    <slot name="tech-stack" slot="tech-stack"></slot>
    <slot name="key-features" slot="key-features"></slot>
    <slot name="role" slot="role"></slot>
    <slot name="development-period" slot="development-period"></slot>
    <slot name="outcome" slot="outcome"></slot>
    <slot name="challenges" slot="challenges"></slot>
</Modal>

<style>
    .link {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background: var(--background-color-2);
        border-radius: 5px;
        box-shadow: 0 0 1rem rgba(0, 0, 0, 0.1);
        overflow: hidden;
        transition: transform 0.3s;
    }
    .link:hover {
        transform: scale(1.05);
    }

    .image {
        flex: none;
        width: 100%;
        height: 180px;
        display: flex;
        justify-content: center;
        align-items: center;
        background: var(--background-light);
        overflow: hidden;
    }

    .image img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .text {
        flex: 1;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        gap: 5px;
        padding: 20px;
    }

    .text > h4 {
        width: 100%;
        display: flex;
        justify-content: flex-start;
        align-items: flex-end;
        gap: 5px;
        font-size: 18px;
        text-transform: uppercase;
    }

    .text > a {
        font-size: 10px;
        text-transform: none;
        text-decoration: none;
        color: var(--text-color-3);
    }
    a:hover {
        opacity: 1;
        text-decoration: underline;
    }

    hr {
        width: 100%;
        height: 1px;
        background: var(--text-color-3);
        opacity: 0.25;
    }

    .tags {
        width: 100%;
        font-size: 10px;
        white-space: nowrap;
        margin: 4px 0;
        overflow: hidden;
        text-overflow: ellipsis;
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
        margin: 0 2px 0 0;
        pointer-events: none;
    }

    .summary {
        flex: 1;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        gap: 5px;
    }
    .summary > p {
        font-size: 12px;
        color: var(--text-color-2);
        opacity: 0.75;
    }

    .expand {
        width: 100%;
        height: 40px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 12px;
    }
    .expand:hover {
        background: var(--background-color);
    }

    p {
        font-size: 14px;
    }

    @media print {
        .link {
            display: none;
        }
    }
</style>