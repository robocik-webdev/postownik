<script>
  import List from './Panels/List.svelte';
  import { authenticated } from './store.js';
  $: console.log($authenticated);
</script>

{#if $authenticated}
  <List />
{/if}
