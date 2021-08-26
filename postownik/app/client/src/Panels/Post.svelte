<script>
</script>

<div class="backgroundlayer">
  <div class="content">
    <div class="content--main">
      <h3>Postownik</h3>
    </div>
    <div class="content--title">
      <input class="title" type="text" placeholder="lorem" />
    </div>
    <div class="content--textarea">
      <textarea
        class="textarea"
        wrap="hard"
        rows="15"
        cols="55"
        placeholder="ipsum"
      />
    </div>

    <!-- Tutaj będą tagi/statusty, kiedyś, szybko, niedługo, soon ( ͡° ͜ʖ ͡°)-->
    <div class="content--buttons">
      <div class="buttonset--small">
        <button class="buttonSmall">Potencjalny post</button>
        <button class="buttonSmall">Post</button>
      </div>
      <div class="buttonset--save">
        <button class="buttonSave">Zapisz</button>
      </div>
    </div>
  </div>
</div>

<style>
  h3 {
    padding: 0;
    margin: 0;
  }

  .backgroundlayer {
    margin: 10px 100px 10px 100px;
  }

  .content {
    width: 600px;
    color: var(--light);
  }

  .content--main,
  .content--title,
  .content--buttons,
  .content--textarea {
    width: 100%;
    cursor: default;
    margin: 5px 0;
  }
  .title {
    position: static;
    outline: none;
    resize: none;
    font-family: inherit;
    width: 250px;
    padding: 4px;
    border: 1px solid var(--grey);
    border-radius: 0;
    cursor: inherit;
    background-color: var(--light);
    color: black;
  }

  .textarea {
    position: static;
    box-shadow: inherit;
    line-height: 1.5;
    border: 1px solid var(--grey);
    outline: none;
    resize: none;
    width: 100%;
    padding: 4px;
    font-family: inherit;
    background-color: var(--light);
  }

  .buttonset--small {
    width: 223px;
    margin-bottom: 5px;
  }
  .buttonset--save {
    width: 223px;
  }

  .buttonSave {
    width: 100%;
  }
</style>
