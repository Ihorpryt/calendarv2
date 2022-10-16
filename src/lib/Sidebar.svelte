<script>
import SvelteTooltip from "./SvelteTooltip.svelte";

    let open = false;
    $: console.log(open)

    function onKeydown(e) {
        if (e.keyCode === 219) {
            open = !open
        }
    }
</script>
  
<!-- svelte-ignore a11y-click-events-have-key-events -->
<nav class:open={open}  on:click={() => open = !open} >
    <!-- Collapse button -->
    <div class="collapse-btn-wrapper">
        <SvelteTooltip tip={open ? "Collapse" : "Expand"} right color="black">
            <div class="collapse-btn"></div>
        </SvelteTooltip>
    </div>
    <!-- Collapse button -->
   

</nav>

<svelte:window on:keydown={onKeydown} />
  
<style>

    nav {
        position: relative;
        min-width: 60px;
        width: 60px;
        background: #888888;
        height: 100vh;
        transition: 0.3s ease-in-out;
    }
    
    .open {
        width: 250px;
    }
    nav:hover .collapse-btn {
        opacity: 1;
    }
    .collapse-btn-wrapper {
        top: 44px;
        right: -12px;
        position: absolute;
    }
    .collapse-btn {
        width: 24px;
        height: 24px;
        border-radius: 50px;
        background-color: white;
        transition: 0.3s ease-in-out;
        opacity: 0;
        z-index: 10;
    }
    :global(body.dark-mode) nav {
        background: #17181C;
        border-right: 0.5px solid rgba(255, 255, 255, 0.1);
    }

</style>