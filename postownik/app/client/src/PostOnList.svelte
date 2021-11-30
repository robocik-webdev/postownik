<script>

    export let title;
    export let content;
    export let type;
    export let visible = true;
</script>
{#if visible}
<div class="post {type}">
    <h2>{title}</h2>
    <p>{content}</p>
    <div class="photo">
    <img src="https://ocdn.eu/pulscms-transforms/1/J8dk9kpTURBXy80ZTRiYzliODhiNzJmOGEzNmM2ZTdjMmI2ZTAzMTJiNi5qcGeTlQPNAggnzQT8zQLPkwXNAxTNAbyTCaY2NWI3MjMGgaEwAQ/mariusz-pudzianowski.jpg" alt="">
</div>
</div>
{:else}
<div class="post invisible {type}">
    <h2>{title}</h2>
    <p>{content}</p>
    <div class="photo">
    <img src="https://ocdn.eu/pulscms-transforms/1/J8dk9kpTURBXy80ZTRiYzliODhiNzJmOGEzNmM2ZTdjMmI2ZTAzMTJiNi5qcGeTlQPNAggnzQT8zQLPkwXNAxTNAbyTCaY2NWI3MjMGgaEwAQ/mariusz-pudzianowski.jpg" alt="">
</div>
</div>
{/if}






<style>
    div.post {
        min-width: 80vw;
        height:80vw;
        position: relative;
        overflow: hidden;
        margin: 20px;
        border: 3px solid white;
        padding: 35px;
        border-radius: 35px;
        
    }
    
    div.private{
        border-color: rgb(50, 50, 50);
    }
    div.concept {
        border-color: purple;
    }
    div.inEdition{
        border-color: orange;
    }
    div.forReview {
        border-color: red ;
    }
    div.ready {
        border-color: blue;
    }
    div.published{
        border-color: green;
    }
    div.invisible{
        display: none;
    }
    h2{
        text-align: center;
        border-bottom: 2px solid white;
        text-transform: uppercase;
        padding: 3px;
    }
    div.photo{
        position: absolute;
        width: 100%;
        height: 30%;
        background-color: rgba(0, 0, 0, 0.8);
        bottom: 0;
        left: 50%;
        transform: translateX(-50%);
        text-align: center;
    }
    img{
        height:100%;
        text-align: center;
    }
    @media (min-width: 400px){
        div.post {
        min-width: 60vw;
        height:60vw;
        
    }
    }
    @media (min-width: 730px){
        div.post {
        width: 400px;
        min-width: 400px;
        height:400px;
        border-width: 5px;
        
    }
    }
</style>