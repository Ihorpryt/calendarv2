<script>
    import ChevronDown from "./Icons/ChevronDown.svelte";

</script>
<div class="user-selector">
    <div class="user">CL</div>
    <div class="details">
        <p>N849WC</p>
        <p class="description">Agusta Helicopter</p>
    </div>
    <ChevronDown />
</div>

<style>
    .user-selector {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 8px;
        margin-left: 16px;
        /* width: 175px; */
    }
    .user {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        min-width: 32px;
        height: 32px;
        background-color: #939393;
        border-radius: 100px;
        color: white;

        font-family: 'Inter Tight';
        font-style: normal;
        font-weight: 400;
        font-size: 12px;
        line-height: 24px;
    }
    .details {
        display: flex;
        flex-direction: column;

        font-family: 'Inter Tight';
        font-style: normal;
        font-weight: 400;
        font-size: 14px;
        line-height: 14px;
        gap: 4px;
        color:black;
        transition: 0.3s;
        width: 100%;
    }
    p {
        margin: 0;
    }

    .description {
        font-size: 12px;
        line-height: 12px;
        color: gray;
    }
    :global(body.dark-mode) .details {
        color:white;
    }
</style>