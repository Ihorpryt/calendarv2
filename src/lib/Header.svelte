<script>
    import DarkModeSwitch from "./DarkModeSwitch.svelte";

</script>


<header>
    <p>Calendar</p>
    <DarkModeSwitch>M</DarkModeSwitch>
</header>

<style>
    header {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        min-height: 56px;
        height: 56px;
        background: #BDBDBD;
        padding-left: 24px;
        padding-right: 24px;
        transition: 0.3s;
    }
    p {
        font-family: 'Inter Tight', sans-serif;
        color: black;
        transition: 0.3s;
    }


	:global(body.dark-mode) header {
		background-color: #1A1B20;
        /* border-bottom: 0.5px solid rgba(255, 255, 255, 0.1); */
		color: #bfc2c7;
	}
    :global(body.dark-mode) p {
		color: #bfc2c7;
	}
</style>