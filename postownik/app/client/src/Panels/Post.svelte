<script>
</script>

<div class="postownik__backgroundlayer">
  <div class="postownik__content">
    <div class="postownik__content--main">
      <h3>Postownik</h3>
    </div>
    <div class="postownik__content--title">
      <input class="postownik--title" type="text" placeholder="lorem" />
    </div>
    <div class="postownik__content--textarea">
      <textarea
        class="postownik--textarea"
        wrap="hard"
        rows="15"
        cols="55"
        placeholder="ipsum"
      />
    </div>
  </div>
</div>

<style>
  h3 {
    padding: 0;
    margin: 0;
  }

  .postownik__backgroundlayer {
    margin: 10px 200px;
  }

  .postownik__content {
    width: 600px;
    color: var(--light);
  }

  .postownik__content--main,
  .postownik__content--title,
  .postownik__content--textarea {
    width: 100%;
    cursor: default;
    margin:5px 0;
  }
  .postownik--title {
    position: static;
    outline: none;
    resize: none;
    font-family: inherit;
    width: 250px;
    padding:4px;
    border: 1px solid var(--grey);
    border-radius: 0;
    cursor: inherit;
    background-color: var(--light);
    color:black;
  }

  .postownik--textarea {
    position: static;
    box-shadow: inherit;
    line-height: 1.5;
    border: 1px solid var(--grey);
    outline: none;
    resize: none;
    width: 100%;
    padding:4px;
    font-family: inherit;
    background-color: var(--light);
  }
</style>
