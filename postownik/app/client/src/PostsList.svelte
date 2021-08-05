<script>
    import PostOnList from './PostOnList.svelte'
    let posts = [];
</script>


<!-- {#each posts as post}
    <PostOnList title = "tytuł" content = "content"/>
{/each} -->
<div class="list">
    <button>Kalendarz</button>
    <h2>Filtrowanie</h2>
    <input type="text">
    <section class="slider">
        <section class="slider__posts">
            <PostOnList title = "tytuł" content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum." type = "concept"/>
            <PostOnList title = "tytuł" content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum." type = "potential"/>
            <PostOnList title = "tytuł" content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum." type = "final"/>
            </section>
    </section>
    </div>

<style>
.slider__posts {
  display: flex;
  overflow-x: auto;
  flex-wrap: nowrap;
  flex-direction: row-reverse;
  align-items: center;
  padding-bottom: 30px;
  margin-top: 30px;
  width: auto;
  transition: transform 200ms;
}

div.list{
  margin: 30px;
}
button{
  color: black;
  font-size: 25px;
  margin-bottom: 20px;
}
h2{
  font-size: 28px;
  margin: 5px 0;
}
input{
  width: 100%;
  margin-bottom: 30px;
}
@media (min-width:1024px){
    input{
        width: 60%;
    }
}


</style>

