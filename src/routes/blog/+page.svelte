<script>
    /** @type {import('./$types').PageData} */
    export let data;
</script>

<div class="container flex items-start justify-center h-full mx-auto">
	<div class="w-5/6">
		<h1 class="m-10 font-extrabold h1 lg:h-28 sm:h-full gradient-heading-2 lg:text-8xl">
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
