<script>
    export let date;
    export let notActive;
    export let current;
</script>

<div class="cell" class:not-active={notActive} class:current={current}>
    <p>{date}</p>
</div>

<style>
    .cell {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        justify-content: flex-start;
        background: #EEEEEE;
        /* padding: 10px; */
        border-right: 0.5px solid grey;
        border-bottom: 0.5px solid grey;
        transition: 0.3s;
        cursor: pointer;
    }
    .cell p {
        margin: 0;
        font-family: 'Inter Tight', sans-serif;
        color: black;
        transition: 0.3s;
        font-size: 16px;
        line-height: 16px;
        width: 26px;
        height: 26px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        /* border-radius: 100px; */
        border-bottom-left-radius: 8px;
    }
    .current p {
        color: white;
        background-color: #01ADF5;
    }
    .not-active p {
        color: gray;
    }
    :global(body.dark-mode) .cell {
        background: #131419;
        border-color: black;
    }
    :global(body.dark-mode) .cell:hover {
        background: #1A1B20;
        border-color: black;
    }
    :global(body.dark-mode) p {
        color: white;
    }
    :global(body.dark-mode) .not-active p {
        color: grey;
    }
    
</style>  