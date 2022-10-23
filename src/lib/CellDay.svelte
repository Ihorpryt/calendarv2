<script>
    export let day;
</script>

<div class="cell">
    <p>{day}</p>
</div>

<style>
    .cell {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        background: #EEEEEE;
        padding: 6px 10px;
        /* border-right: 0.5px solid grey; */
        border-bottom: 0.5px solid grey;
        transition: 0.3s;
    }
    .cell p {
        margin: 0;
        font-family: 'Inter Tight', sans-serif;
        color: grey;
        font-size: 12px;
        line-height: 16px;
        transition: 0.3s;
    }
    :global(body.dark-mode) .cell {
        background: #131419;
        border-color: black;
    }
    
</style>  