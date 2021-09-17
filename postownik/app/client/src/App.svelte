<script>
  import List from './Panels/List.svelte';
  import Calendar from './Panels/Calendar.svelte'; 
  import { authenticated } from './store.js';
  $: console.log($authenticated);
</script>



<Calendar/>

<!-- {#if $authenticated}
  <List />
{/if} -->
