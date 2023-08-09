<script>
    /** @type {import('./$types').PageData} */
    export let data;
    const { title, date, Content } = data
</script>

<article class="container h-full mx-auto flex flex-col justify-center items-center space-y-5">
  <h1 class="h1">{title}</h1>
  <p>Published: {date}</p>
  <Content />
</article>