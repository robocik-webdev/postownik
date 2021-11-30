<script>
    import PostOnList from './PostOnList.svelte'
    let posts = [
      {title: "tytuł", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum.", type: "ready", visible: true},
      {title: "tytuł", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum.", type: "forReview", visible: true},
      {title: "tytuł", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum.", type: "published", visible: true},
      {title: "tytuł", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum.", type: "inEdition", visible: true},
      {title: "tytuł", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum.", type: "private", visible: true},
      {title: "tytuł", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum.", type: "private", visible: true},
      {title: "tytuł", content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum.", type: "concept", visible: true}

      ];
      let selectedType;
        $:{if(selectedType == 0){
          posts.forEach((post) =>{post.visible = true})
        }
        else if(selectedType == 1){
          posts.forEach((post) =>{
            if(post.type != "private")
            post.visible = false
            else
            post.visible = true
          })
        }
        else if(selectedType == 2){
          posts.forEach((post) =>{
            if(post.type != "concept")
            post.visible = false
            else
            post.visible = true
          })
        }
        else if(selectedType == 3){
          posts.forEach((post) =>{
            if(post.type != "inEdition")
            post.visible = false
            else
            post.visible = true
          })
        }
        else if(selectedType == 4){
          posts.forEach((post) =>{
            if(post.type != "forReview")
            post.visible = false
            else
            post.visible = true
          })
        }
        else if(selectedType == 5){
          posts.forEach((post) =>{
            if(post.type != "ready")
            post.visible = false
            else
            post.visible = true
          })
        }
        else if(selectedType == 6){
          posts.forEach((post) =>{
            if(post.type != "published")
            post.visible = false
            else
            post.visible = true
          })
        }
        posts = posts;
      }
</script>


<!-- {#each posts as post}
    <PostOnList title = "tytuł" content = "content"/>
{/each} -->
<div class="list">
    <button>Kalendarz</button>
    <div class="filter">
    <h2>Filtrowanie</h2>
    <label for="status">Status: </label>
    <select bind:value={selectedType} name = "status">
      <option value="0">Wszystkie </option>
      <option value="1">Koncept Prywatny </option>
      <option value="2">Koncept</option>
      <option value="3">W edycji</option>
      <option value="4">Do Przeglądu</option>
      <option value="5">Gotowy</option>
      <option value="6"> Opublikowany</option>
    </select>
  </div>
    <section class="slider">
        <section class="slider__posts">
            <!-- <PostOnList title = "tytuł" content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum." type = "private"/>
            <PostOnList title = "tytuł" content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum." type = "concept"/>
            <PostOnList title = "tytuł" content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum." type = "inEdition"/>
            <PostOnList title = "tytuł" content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum." type = "forReview"/>
            <PostOnList title = "tytuł" content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum." type = "ready"/>
            <PostOnList title = "tytuł" content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis nisl id erat mattis maximus. Phasellus porta nibh sed dapibus finibus. Nam purus urna, hendrerit vel maximus ac, ultricies nec purus. Maecenas tempus lectus dui, ut pretium nunc viverra eget. Vivamus mollis dolor in enim dignissim imperdiet. Maecenas dui arcu, pulvinar vitae nunc eget, dignissim aliquam lacus. Quisque consectetur sollicitudin lacus ac euismod. Donec feugiat orci at elit semper, accumsan maximus massa consectetur. Donec ultrices risus justo, eget consectetur odio dapibus at. Curabitur purus odio, posuere quis ligula a, tincidunt faucibus ante. Sed dignissim est sit amet vehicula sollicitudin. Nullam sollicitudin quis neque in dictum." type = "published"/> -->
            {#each posts as post}
            <PostOnList {...post}/>
            {/each}
            </section>
    </section>
    </div>

<style>
.slider__posts {
  display: grid;

  /* overflow-x: auto; */
  /* flex-wrap: nowrap;
  flex-direction: column; */
  /* align-items: center; */
  /* grid-template-columns: repeat(2,40%); */
  justify-content: center;
  padding-bottom: 30px;
  margin: auto;
  margin-top: 30px;
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
select{
  width: 100%;
  margin-bottom: 30px;
  font-size: 18px;
}
label{
  font-size:22px;
  margin-right: 10px;
}
@media (min-width: 600px) {
  select{
        width: 50%;
        font-size: 20px;
    }
    
}
@media (min-width:1024px){
    select{
        width: 30%;
    }
    
.slider__posts{
  grid-template-columns: repeat(2,50%);
}
}
@media (min-width: 1248px){
  div.filter{
  position: sticky;
  top: 20px;
  width: 40%;
}
.slider__posts{
  grid-template-columns: repeat(2,40%);
  justify-content: end;
}
}


</style>

