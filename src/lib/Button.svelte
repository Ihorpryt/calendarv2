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
        font-weight: 500;
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
        background: rgba(255, 255, 255, 0.04);
        border-color: rgba(255, 255, 255, 0);
    }
    :global(body.dark-mode) .secondary:hover {
        background: rgba(255, 255, 255, 0.1);
    }
    :global(body.dark-mode) .primary {
        background: #01ADF5;
        color: white;
    }
    :global(body.dark-mode) .chevron-left {
        border-right: 0.5px solid #131419;
    }

</style>
