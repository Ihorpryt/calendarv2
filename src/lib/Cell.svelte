<script>
    export let date;
    export let notActive;
</script>

<div class="cell" class:not-active={notActive}>
    <p>{date}</p>
</div>

<style>
    .cell {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;
        background: #EEEEEE;
        padding: 10px;
        border-right: 0.5px solid grey;
        border-bottom: 0.5px solid grey;
        transition: 0.3s;
    }
    .cell p {
        margin: 0;
        font-family: 'Inter Tight', sans-serif;
        color: black;
        transition: 0.3s;
    }
    .not-active p {
        color: gray;
    }
    :global(body.dark-mode) .cell {
        background: #131419;
        border-color: black;
    }
    :global(body.dark-mode) p {
        color: white;
    }
    :global(body.dark-mode) .not-active p {
        color: grey;
    }
    
</style>  