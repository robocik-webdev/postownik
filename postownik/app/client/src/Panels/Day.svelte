<script>
import { get } from "svelte/store";


    export let date = new Date();
    export let isCurrentMonth;
    let currentDate = new Date();
    function checkifDayIsToday(date1, date2){
        return (date1.getDate() == date2.getDate() && date1.getMonth() ==date2.getMonth() && date1.getFullYear() == date2.getFullYear())
    }

</script>
{#if isCurrentMonth == false}
<div class="previous"><p>{date.getDate()}</p></div>
{:else if checkifDayIsToday(currentDate, date)}
    <div class="today"><p>{date.getDate()}</p></div>
{:else}
    <div ><p>{date.getDate()}</p></div>
{/if}
<style>
    div{
        height: 100px;
        border-top: 1px solid black;
        border-right: 1px solid black;
        padding: 10px;
    }
    p{
        font-size: 20px;
        margin: 0;
    }
    div.previous{
        color: brown;
        background-color: #021031;
    }
    div.today{
        color: green;
    }
</style>
