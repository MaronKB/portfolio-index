<script lang="ts">
    export let name: string;
    export let image: string;
    export let percentage: string;
    export let list: string[];
</script>

<div class="skill">
    <div class="skill-field"
         style={`background: conic-gradient(white ${percentage}%, #aaaaaa77 ${percentage}%)`}>
        <div class="skill-img-container">
            <img class="skill-img" src={image} alt={name}/>
        </div>
        <h3 class="skill-name">{name}</h3>
    </div>
    <div class="skill-ability">
        <div class="skill-ruler">
            <span class="skill-limit">미숙</span>
            <span class="skill-limit">기초</span>
            <span class="skill-limit">숙련</span>
            <span class="skill-limit">완숙</span>
            <span class="skill-limit">대성</span>
        </div>
        <progress class="skill-progress" max="100" value={percentage}></progress>
        <ul class="skill-desc">
            {#each list as li}
                <li>{@html li}</li>
            {/each}
        </ul>
    </div>
</div>

<style>
    .skill {
        flex: none;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 10px;
    }
    @media (max-width: 600px) {
        .skill {
            flex-direction: column;
            gap: 20px;
        }
    }
    .skill-field {
        position: relative;
        flex: none;
        width: 80px;
        height: 80px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        border-radius: 50%;
        padding: 8px;
        margin: auto 0;
    }
    .skill-img-container {
        flex: none;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        background: white;
        padding: 10px;
        border-radius: 50%;
        box-shadow: 0 0 5px #0003;
        overflow: hidden;
    }
    .skill-img {
        flex: none;
        width: 100%;
        height: 100%;
        object-fit: contain;
    }
    .skill-name {
        position: absolute;
        bottom: 0;
        transform: translateY(50%);
        flex: none;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 80%;
        text-align: center;
        line-height: 100%;
        color: var(--text-color-3);
        background: var(--background-color);
        padding: 2px 6px;
    }
    .skill-ability {
        flex: 1;
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 5px;
        overflow: hidden;
        transition: flex 0.3s;
    }
    .skill-ability .skill-ruler {
        flex: none;
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-size: 9px;
    }
    .skill-ability .skill-progress {
        flex: none;
        width: 100%;
        border-radius: 5px;
        overflow: hidden;
        appearance: none;
    }
    .skill-ability .skill-progress::-webkit-progress-bar {
        background: var(--background-color-3);
    }
    .skill-ability .skill-progress::-webkit-progress-value {
        background: var(--text-color-3);
    }
    .skill-desc {
        flex: 1;
        width: 100%;
        font-size: 13px;
        line-height: 16px;
        background: var(--background-color);
        box-shadow: 0 0 5px #0003 inset;
        padding: 10px;
        border-radius: 3px;
        margin: 0;
        list-style: none;
    }
    .skill-desc li {
        padding: 0 0 0 15px;
        margin: 4px 0;
    }
    .skill-desc li::before {
        content: "•";
        color: var(--text-color-3);
        display: inline-block;
        width: 1em;
        margin-left: -1em;
    }
</style>