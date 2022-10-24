<script>  
    import Button from "./Button.svelte";
    import Cell from "./Cell.svelte";
    import CellDay from "./CellDay.svelte";
    import ChevronLeft from "./Icons/ChevronLeft.svelte";
    import ChevronRight from "./Icons/ChevronRight.svelte";
    import FilterIcon from "./Icons/FilterIcon.svelte";
    import Legend from "./Icons/Legend.svelte";
    import PlusIcon from "./Icons/PlusIcon.svelte";
    import Print from "./Icons/Print.svelte";
    
    let hasClass = document.body.classList.contains('dark-mode');

    const days = [
        {day: 'Sunday'},
		{day: 'Monday'},
        {day: 'Tuesday'},
        {day: 'Wednesday'},
        {day: 'Thursday'},
        {day: 'Friday'},
        {day: 'Saturday'},
    ];


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
                    <ChevronRight />
                </Button>
            </div>
                <h2>October 2022</h2>
        </div>

        <div class="right">
            <Button variant="secondary"> 
                <Print/> 
            </Button>
            <Button variant="secondary"> 
                <Legend/> 
            </Button>
            <Button variant="secondary"> 
                <FilterIcon/> 
            </Button>
            <Button variant="primary"> 
                <PlusIcon color="white"/> 
                Add event
            </Button>
        </div>
    </div>
    <div class="grid">
        {#each days as {day}}
            <CellDay day={day} />
        {/each}
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
        margin-left: 24px;
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
        min-height: 56px;
        height: 56px;
        background: #D9D9D9;
        padding: 0 24px;
        transition: 0.3s;
    }
    .navigator {
        display: flex;
        flex-direction: row;
        margin-left: 8px;
    }
    .left {
        display: flex;
        flex-direction: row;
        align-items: center;
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
        grid-template-rows: auto 1fr 1fr 1fr 1fr 1fr 1fr;
        height: 100%;
        width: 100%;
        border-top: 0.5px solid grey;
    }

    :global(body.dark-mode) h2 {
        color: white;
    }
    :global(body.dark-mode) .sub-panel {
		background: #131419;
	}
    :global(body.dark-mode) .grid {
        border-color: black;
    }
</style>  