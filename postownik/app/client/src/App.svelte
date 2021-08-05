<script>
  import List from './Panels/List.svelte';
  import PostsList from './PostsList.svelte';
  import { authenticated } from './store.js';
  $: console.log($authenticated);
</script>
<PostsList/>



{#if $authenticated}
  <List />
{/if}



