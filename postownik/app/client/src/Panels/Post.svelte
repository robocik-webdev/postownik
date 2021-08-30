<script>
</script>

<div class="backgroundlayer">
  <div class="main">
    <div class="content">
      <h3>Postownik</h3>
    </div>
    <div class="content">
      <input class="title" type="text" placeholder="lorem" />
    </div>
    <div class="content">
      <textarea
        class="textarea"
        wrap="hard"
        rows="15"
        cols="55"
        placeholder="ipsum"
      />
    </div>
    <div class="content">
      <div class="tagi">
        <input />
      </div>
      <div class="status">
        <select class="statusList">
          <option>-- zmień status postu --</option>
          <option style="color:violet">Koncept</option>
          <option style="color:orange" disabled>W edycji</option>
          <option style="color:red">Do przeglądu</option>
          <option style="color:blue">Gotowy</option>
        </select>
      </div>
    </div>
    <div class="content">
      <div class="buttonsetSmall">
        <button class="btnSmall">Potencjalny post</button>
        <button class="btnSmall">Post</button>
      </div>
      <div class="buttonsetSave">
        <button class="btnSave">Zapisz</button>
      </div>
    </div>
  </div>
</div>

<style>
  option {
    cursor: pointer;
  }

  option[disabled] {
    background-color: var(--grey);
  }

  .backgroundlayer {
    margin: 10px 100px 10px 100px;
  }

  .main {
    width: 600px;
    color: var(--light);
  }

  .content {
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

  .tagi input {
    width: 402px;
  }

  .tagi,
  .status {
    display: inline;
  }

  .buttonsetSmall {
    width: 223px;
    margin-bottom: 5px;
  }
  .buttonsetSave {
    width: 223px;
  }

  .btnSave {
    width: 100%;
  }
</style>
