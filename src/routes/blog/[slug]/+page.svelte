<script>
    /** @type {import('./$types').PageData} */
    export let data;
    const { title, date, Content } = data
</script>

<article class="container h-full mx-auto flex flex-col items-center">
  <h1 class="h1 lg:h-28 sm:h-full font-extrabold gradient-heading-2 text-8xl m-10">
    {title}
  </h1>
  <div class="w-5/6 prose dark:prose-invert text-justify">
    <Content />
  </div>
  <br>
  <br>
  <!-- <p class="text-sm">Published: {date}</p> -->
  <br>
</article>