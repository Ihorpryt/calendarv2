<script>
    import Button from "./Button.svelte";
    import Cell from "./Cell.svelte";
    import ChevronLeft from "./Icons/ChevronLeft.svelte";
    import ChevronRight from "./Icons/ChevronRight.svelte";
    import FilterIcon from "./Icons/FilterIcon.svelte";
    import PlusIcon from "./Icons/PlusIcon.svelte";
    
    let hasClass = document.body.classList.contains('dark-mode');


</script>

<section>
    <div class="sub-panel">
        <div class="left">
            <Button variant="secondary"> 
                Today
            </Button>
            <div class="navigator">
                <Button variant="secondary chevron-left"> 
                    <ChevronLeft />
                </Button>
                <Button variant="secondary chevron-right"> 
                    <ChevronRight color="" />
                </Button>
            </div>
                <h2>October 2022</h2>
        </div>

        <div class="right">
            <Button variant="secondary"> 
                <FilterIcon color=""/> 
            </Button>
            <Button variant="primary"> 
                <PlusIcon color="white"/> 
                Add event
            </Button>
        </div>
    </div>
    <div class="grid">
        {#each Array(3) as _, index (index)}
            <Cell date={index+28} notActive={true} />
        {/each}
        {#each Array(31) as _, index (index)}
            <Cell date={index+1} notActive={false} />
        {/each}
        {#each Array(8) as _, index (index)}
            <Cell date={index+1} notActive={true} />
        {/each}
    </div>
</section>

<style>
    h2 {
        font-family: 'Inter Tight';
        font-style: normal;
        font-weight: 400;
        font-size: 22px;
        line-height: 30px;
        color: #000000;
    }
    section {
        display: flex;
        flex-direction: column;
        width: 100%;
        height: 100%;
    }
    .sub-panel {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        height: 60px;
        background: #D9D9D9;
        padding: 0 24px;
        transition: 0.3s;
    }
    .navigator {
        display: flex;
        flex-direction: row;
    }
    .left {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 24px;
    }
    .right {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 8px;
    }
    .grid {
        display: grid;
        grid-template-columns: repeat(7, 1fr);
        height: 100%;
        width: 100%;
        border-top: 0.5px solid grey;
    }

    :global(body.dark-mode) .sub-panel {
		background: #131419;
	}
    :global(body.dark-mode) .grid {
        border-color: black;
    }
</style>  