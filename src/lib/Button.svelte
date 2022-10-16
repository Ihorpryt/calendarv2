<script>
    export let variant;
    
</script>

<button type="button" class="{variant}"><slot></slot></button>

<style>
    button {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap:8px;
        border-radius: 8px;
        height: 36px;
        cursor: pointer;

        font-family: 'Inter Tight';
        font-style: normal;
        font-weight: 400;
        font-size: 14px;
        line-height: 17px;
        border: none;
        padding: 0 12px;
        transition: 0.3s;
    }
    
    .primary {
        background: black;
        transition: 0.3s;
    }
    .primary:hover {
        background: #333;
    }
    .secondary {
        color: black;
        background: none;
        transition: 0.3s;
        border: 0.5px solid #FFF;
    }
    .secondary:hover {
        color: black;
        background: #BDBDBD;
    }
    .chevron-left {
        border-top-right-radius: 0px;
        border-bottom-right-radius: 0px;
    }
    .chevron-right {
        border-top-left-radius: 0px;
        border-bottom-left-radius: 0px;
        border-left: 0px solid;
    }

    :global(body.dark-mode) .secondary {
        color: white;
    }
    :global(body.dark-mode) .primary {
        background: #01ADF5;
        color: white;
    }

</style>
