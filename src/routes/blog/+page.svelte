<script>
    /** @type {import('./$types').PageData} */
    export let data;
</script>

<div class="container h-full mx-auto flex justify-center items-start">
	<div class="">
		<h1 class="h1 font-extrabold text-transparent text-6xl bg-clip-text bg-gradient-to-r from-purple-400 to-pink-600 m-10">Blogging like it's 2008</h1>
        <ul>
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
