<script>
  import Postownik from './Panels/Post.svelte';
  import { authenticated } from './store.js';
  $: console.log($authenticated);
</script>

<Postownik />

<style>
</style>
