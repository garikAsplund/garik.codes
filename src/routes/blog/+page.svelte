<script>
    /** @type {import('./$types').PageData} */
    export let data;
</script>

<div class="container flex items-start justify-center h-full mx-auto">
	<div class="translate-y-12 seven text-token w-5/6">
		<h1 class="m-10 font-mono font-light lg:text-6xl md:text-4xl">
      Blogging like it's 2008
    </h1>
      <ul class="mx-24 space-y-5">
        {#each data.posts as post}
          <li>
            <h2 class="h2">
              <a class="hover:underline" href={post.path}>
                {post.meta.title}
              </a>
            </h2>
            &nbsp&nbsp&nbsp{post.meta.date}
          </li>
        {/each}
      </ul>
  </div>
</div>

<style>
.seven h1 {
  text-align: center;
      /* font-size:5rem; font-weight:300; letter-spacing:1px; */
      text-transform: uppercase;
  
      display: grid;
      grid-template-columns: 1fr max-content 1fr;
      grid-template-rows: 27px 0;
      grid-gap: 20px;
      align-items: center;
  }
  
  .seven h1:after,.seven h1:before {
      content: " ";
      display: block;
      border-bottom: 1px solid;
      border-top: 1px solid;
      height: 0.7rem;
    background-color:transparent;
  }
</style>
