<script>
import { attr } from "svelte/internal";


  let status = [
    { id: 'default', value: '-- zmień status postu --' },
    { id: 'koncept', value: 'Koncept'},
    { id: 'edycja', value: 'W edycji'},
    { id: 'przeglad', value: 'Do przeglądu' },
    { id: 'gotowy', value: 'Gotowy' }
  ];

  let selected = 'default';

 
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
      <div class="drop-zone" />
    </div>
    <div class="content">
      <div class="tag">
        <input />
      </div>
      <div class="status">
        <select class="statusList" bind:value={selected}>
          {#each status as status}
            <option value={status.id}>{status.value}</option>>
          {/each}
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
    width: 600px;
    cursor: default;
    margin: 5px;
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
    outline: none;
    resize: none;
    width: 600px;
    font-family: inherit;
    background-color: var(--light);
  }

  .tag input {
    width: 359px;
  }

  .tag,
  .status {
    display: inline;
  }

  .drop-zone {
    height: 150px;
    border: 2px dashed var(--grey);
    border-radius: 15px;
    cursor: pointer;
    margin-bottom: 10px;
  }

  .content .buttonsetSmall {
    display: inline;
  }

  .btnSave {
    width: 260px;
    margin-top: 5px;
  }
</style>
