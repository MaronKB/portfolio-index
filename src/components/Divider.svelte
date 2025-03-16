<script lang="ts">
    import Logo from '/src/assets/logo.svg?raw';
</script>
<div class="divider">
    <div class="logo">
        <i>{@html Logo}</i>
    </div>
</div>
<style>
    .divider {
        width: 100%;
        height: 2px;
        display: flex;
        justify-content: center;
        align-items: center;
        background: linear-gradient(to right, transparent, var(--text-color-3) calc(50% - 25px) calc(50% + 25px), transparent);
        margin: 20px 0;
    }
    .logo {
        width: 40px;
        height: 40px;
        display: flex;
        justify-content: center;
        align-items: center;
        background: var(--text-color-3);
        transform: rotate(45deg);
    }
    .logo > i {
        width: 25px;
        height: 25px;
        display: flex;
        justify-content: center;
        align-items: center;
        fill: var(--background-color);
        object-fit: contain;
        transform: rotate(-45deg);
    }
</style>