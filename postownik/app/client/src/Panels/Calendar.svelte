<script>
import Day from './Day.svelte'
let monthNames = ["Styczeń", "Luty", 'Marzec', "Kwiecień", "Maj", "Czerwiec", "Lipiec", "Sierpień", "Wrzesień", "Październik", "Listopad", "Grudzień"];
let currentDate = new Date();
let chosenDate = currentDate;
let chosenMonth =chosenDate.getMonth() ;
let daysInMonth = [];

function checkFirstDay(){
        let firstDay = new Date (chosenDate);
        firstDay.setDate(1)
        // console.log(firstDay.getDay())
        return firstDay
    }
    function checkAmountOfDays(month, year){
        // console.log(new Date(year, month + 1, 0).getDate())
        return new Date(year, month +1, 0).getDate();
    }
    function createArrayOfDates(){
        daysInMonth = [];
        for(let i = 0; i < (checkAmountOfDays(chosenDate.getMonth(),chosenDate.getFullYear())) ; i++ ) {
            let tempDate = new Date(checkFirstDay())
            tempDate.setDate(tempDate.getDate()+i)
            daysInMonth.push(tempDate)
            }
            daysInMonth = daysInMonth
 }



function removeMonth(){
    chosenDate.setMonth(chosenDate.getMonth() - 1)
    chosenMonth =chosenDate.getMonth() ;
    createArrayOfDates();
    chosenDate = chosenDate;
   
}
function addMonth(){
    chosenDate.setMonth(chosenDate.getMonth() + 1)
    chosenMonth =chosenDate.getMonth() ;
    createArrayOfDates();
    chosenDate = chosenDate;
}
createArrayOfDates();


</script>

<div class="wrapper">
    <h3 class="year">{chosenDate.getFullYear()}</h3>
<nav>
<button on:click={removeMonth}  class="previous">p</button>
<h1 class="month">{monthNames[chosenMonth%12]}</h1>
<button on:click={addMonth}  class="next">n</button>
</nav>
</div>

<div class="container">
    {#each daysInMonth as dayInMonth}
        <div>{dayInMonth}</div>
    {/each}
    <Day/>
</div>



<style>
    div.wrapper{
        text-align: center;
    }
    nav{
        display: flex;
        padding: 15px;
    }
    h1{
        margin: 15px auto;
    }
</style>