<script>
    export let date = new Date();
    export let isCurrentMonth;

</script>
{#if isCurrentMonth == false}
<div class="previous"><p>{date.getDate()}</p></div>
{:else}
    <div><p>{date.getDate()}</p></div>
{/if}
<style>
    div{
        height: 100px;
        margin: 5px;
        border: 2px solid black;
        padding: 10px;
    }
    p{
        font-size: 20px;
    }
    div.previous{
        color: brown;
        background-color: #021031;
    }
</style>
