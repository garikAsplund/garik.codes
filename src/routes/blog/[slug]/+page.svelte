<script>
    /** @type {import('./$types').PageData} */
    export let data;
    const { title, date, Content } = data
</script>

<article class="container h-full mx-auto flex flex-col items-center">
  <h1 class=" h-28 font-extrabold text-transparent text-4xl md:text-8xl bg-clip-text bg-gradient-to-r from-purple-400 to-pink-600
  m-10">{title}</h1>
  <div class="w-5/6 prose dark:prose-invert text-justify">
    <Content />
  </div>
  <br>
  <br>
  <p class="text-sm">Published: {date}</p>
  <br>
</article>