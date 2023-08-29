<script>
    import { page } from '$app/stores';
</script>
  
<div class="h-full flex items-center justify-center -translate-y-10">
  <!-- <h1 class="text-center">{$page.status} {$page.error.message}</h1> -->
  {#if $page.status === 404}
    <img src="https://i.kym-cdn.com/photos/images/newsfeed/000/236/756/b33.jpg" alt="Page not found, cat not found" title="Nothing to see here" />
  {:else if $page.status === 500}
    <img src="https://http.cat/images/500.jpg" alt="Oh noooo" title="No way" />
  {/if}
</div>