<script>
import Day from './Day.svelte'
let monthNames = ["Styczeń", "Luty", 'Marzec', "Kwiecień", "Maj", "Czerwiec", "Lipiec", "Sierpień", "Wrzesień", "Październik", "Listopad", "Grudzień"];
let currentDate = new Date();
let chosenDate = currentDate;
let chosenMonth =chosenDate.getMonth() ;
let daysInMonth = [];
function checkLastDay(date){
    let lastDay = new Date(date);
    
    lastDay = checkFirstDay(date);
    lastDay.setDate(lastDay.getDate()+1)
   
    lastDay.setMonth(lastDay.getMonth()+1)
    lastDay.setDate(lastDay.getDate()-1)
    console.log(lastDay.getDay())
    
    
    
    
    return lastDay;
}
function checkFirstDay(date){
        let firstDay = new Date (date);
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
        if(checkFirstDay(chosenDate).getDay()==0){
            // console.log("essa")
            for(let i=1;i<7;i++){
            let tempDate = new Date(checkFirstDay(chosenDate))
            console.log(checkFirstDay(chosenDate).getDay()+6)
            tempDate.setDate(tempDate.getDate()-(checkFirstDay(chosenDate).getDay()+7-i))
            
            daysInMonth.push(tempDate)
        }
        }else{
        for(let i=1;i<checkFirstDay(chosenDate).getDay();i++){
            let tempDate = new Date(checkFirstDay(chosenDate))
            tempDate.setDate(tempDate.getDate()-(checkFirstDay(chosenDate).getDay()-i))

            daysInMonth.push(tempDate)
        }
    }
        for(let i = 0; i <(checkAmountOfDays(chosenDate.getMonth(),chosenDate.getFullYear())) ; i++ ) {
            let tempDate = new Date(checkFirstDay(chosenDate))
            tempDate.setDate(tempDate.getDate()+i)

            daysInMonth.push(tempDate)
            }

            if(checkLastDay(chosenDate).getDay()!=1 &&checkLastDay(chosenDate).getDay()!=0){
            for(let i=0; i<=(7-checkLastDay(chosenDate).getDay()); i++){
            let tempDate = new Date(checkLastDay(chosenDate))
            
            tempDate.setDate(tempDate.getDate()+i)

            daysInMonth.push(tempDate)
            
        }
    }
        else if(checkLastDay(chosenDate).getDay()==0){
            let tempDate = new Date(checkLastDay(chosenDate))
            
            tempDate.setDate(tempDate.getDate())

            daysInMonth.push(tempDate)
        }
        // console.log(checkLastDay(chosenDate).getDay());
        //     console.log(7-checkLastDay(chosenDate).getDay());
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
<button on:click={removeMonth}  class="previous"><i class="fas fa-arrow-left"></i></button>
<h1 class="month">{monthNames[chosenMonth%12]}</h1>
<button on:click={addMonth}  class="next"><i class="fas fa-arrow-right"></i></button>
</nav>
</div>

<div class="container">
    <h2>pon</h2>
    <h2>wt</h2>
    <h2>śr</h2>
    <h2>czw</h2>
    <h2>pt</h2>
    <h2>sob</h2>
    <h2>nd</h2>
    {#each daysInMonth as dayInMonth}
    {#if dayInMonth.getMonth() == chosenDate.getMonth()}
    <Day date = {dayInMonth} isCurrentMonth = {true}/>
    {:else}
    <Day date = {dayInMonth} isCurrentMonth ={false}/>
    {/if}
    
    {/each}
  
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
    div.container{
        margin: 10px auto;
        width: 90%;
        display: grid;
        grid-template-columns: repeat(7, calc(1/7 * 100%));
        align-items: center;
        justify-content: center;
        border-left: 1px solid black;
        border-bottom: 1px solid black;
    }
</style>