<script>
  import { attr } from 'svelte/internal';

  let status = [
    { id: 'default', value: 'wybierz' },
    { id: 'koncept', value: 'Koncept' },
    { id: 'edycja', value: 'W edycji' },
    { id: 'gotowy', value: 'Gotowy' },
  ];

  let selected = 'default';
</script>

<div class="backgroundlayer">
  <div class="main">
    <div class="header">
      <img src="./rsc/logo.png" alt="logo" class="headerLogo" />
      <h3>POSTOWNIK</h3>
    </div>
    <div class="contentZone">
      <div class="title">
        <input type="text" class="inputTitle" placeholder="Tytuł" />
      </div>
      <hr />
      <div class="textarea">
        <textarea placeholder="Treść" />
      </div>
    </div>
    <div class="attachmentZone">
      <div class="poteznyPudzianPrzesuwaMojeDivy">
        Załącznik &nbsp;&nbsp;&nbsp;
        <input type="file" id="file" class="attachment" />
        <label for="file" class="dummyAttachment">dodaj</label>
        <div class="fileGallery">
          <div class="file">plik ABC</div>
        </div>
      </div>
    </div>
    <div class="tagZone">
      <div class="poteznyPudzianPrzesuwaMojeDivy">
        Otaguj &nbsp;&nbsp;&nbsp;
        <div class="tags"><input type="text" placeholder="wyszukaj" /></div>
        <div class="tagGallery">
          <div class="tag">tag 1</div>
          <div class="tag">tag 2</div>
          <div class="tag">tag 3</div>
        </div>
      </div>
    </div>
    <div class="status">
      <div class="poteznyPudzianPrzesuwaMojeDivy">
        Status &nbsp;&nbsp;&nbsp;
        <select class="statusList" bind:value={selected}>
          {#each status as status}
            <option value={status.id}>{status.value}</option>
          {/each}
        </select>
      </div>
    </div>
  </div>
  <div class="buttonZone">
    <div class="post">
      <div class="buttonContent">
        <a href="https://www.youtube.com/watch?v=TJoeeTM2o50">Post</a>
      </div>
    </div>
    <div class="spacer" />
    <div class="save">
      <div class="buttonContent">
        <a href="https://www.youtube.com/watch?v=TJoeeTM2o50">Zapisz</a>
      </div>
    </div>
  </div>
</div>

<style>
  .backgroundlayer {
    width: 600px;
    height: 800px;
  }

  .main {
    width: 400px;
    color: white;
    margin: 0px 100px;
    height: 700px;
  }

  .poteznyPudzianPrzesuwaMojeDivy {
    float: right;
    margin: 10px 0 0;
  }

  .header {
    height: 26px;
    width: 100%;
    display: flex;
    margin: 5px 0;
  }

  .headerLogo {
    height: 100%;
    display: inline-block;
    width: 26px;
  }

  .header h3 {
    color: #3b4a76;
    margin-left: 5px;
    padding: 0px;
  }

  .contentZone {
    position: static;
    width: inherit;
    border: 2px solid #6c89bd;
    border-radius: 15px;
  }

  .inputTitle {
    background-color: white;
    border: 0;
    color: #3b4a76;
    cursor: text;
    margin: 0px 12px;
    width: 370px;
    font-size: 20px;
  }

  hr {
    width: 350px;
    margin: 0px 25px;
    border: 1px solid #dce8fc;
  }

  textarea {
    position: static;
    line-height: 1.5;
    padding: 8px;
    outline: none;
    resize: none;
    font-family: inherit;
    background-color: white;
    color: var(--grey);
    border: 0;
    margin: 0px 15px;
    width: 370px;
    height: 400px;
  }

  .inputTitle::placeholder {
    color: #3b4a76;
  }

  textarea::placeholder {
    color: var(--grey);
  }

  .attachmentZone {
    width: 100%;
    color: #3b4a76;
    position: inline-block;
  }

  .attachment {
    display: none;
  }

  .dummyAttachment {
    border: 2px solid #6c89bd;
    padding: 2px 47px;
    border-radius: 10px;
    cursor: pointer;
  }

  .fileGallery {
    margin: 10px 0 0;
  }

  .file {
    color: #90b8fc;
    border: 2px solid #c8dcfd;
    border-radius: 10px;
    padding: 2px 8px;
    margin: 0 0 0 10px;
    float: right;
  }

  .tagZone {
    width: 100%;
    color: #3b4a76;
  }

  .tags {
    display: inline;
  }

  .tags input {
    cursor: text;
    width: 150px;
    border-color: #6c89bd;
    color: #3b4a76;
  }

  .tagGallery {
    margin: 10px 0 0;
  }

  .tag {
    color: #90b8fc;
    border: 2px solid #c8dcfd;
    display: inline-block;
    border-radius: 10px;
    padding: 2px 8px;
    margin: 0 0 0 10px;
  }

  .status {
    width: 100%;
    color: #3b4a76;
  }

  option,
  select {
    color: #3b4a76;
  }

  select {
    border-color: #6c89bd;
    width: 150px;
  }

  .buttonZone {
    width: 100%;
    height: 35px;
    display: inline-flex;
    color: white;
  }

  .buttonZone a {
    text-decoration: none;
    color: white;
    width: 250px !important;
  }
  .post {
    width: 300px;
    height: 100%;
    background-color: #6c89bd;
    border-radius: 0 10px 10px 0;
  }

  .buttonContent {
    width: 100%;
    padding:5px 10px;
  }

  .post .buttonContent{
    margin-left:240px;
  }
  .spacer {
    width: 50px;
    height: 100%;
    background-color: white;
  }

  .save {
    width: 250px;
    height: 100%;
    background-color: #3b4a76;
    border-radius: 10px 0 0 10px;
  }
</style>
