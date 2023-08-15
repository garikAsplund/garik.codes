---
title: Why Svelte?
date: "2023-08-14"
---

## Simplicity > Popularity

When it comes to JavaScript <del>frameworks</del> libraries, **React** is king, and it kinda has been ever since it came out a decade ago. It has the biggest user base as well as the most tools and trinkets to trick out any and every project. 

However, it's 2023 and React is **bloated, complicated, and slow**.

![React on top](../svelte.png "React wins the popularity contest")

That's not really a secret, and it feels like over the last few years React has become a punching bag. Fortunately, there are other--[arguably too many](https://krausest.github.io/js-framework-benchmark/2023/table_chrome_116.0.5845.82.html)--frameworks and libraries that are seeking solutions. Some of these solutions are super slick, others not so much. Frameworks written in Rust, like Yew, can be just as bad as React. Others, written in TypeScript, like Solid, *kill* when it comes to speed. So, which framework is best?

**Svelte, and now SvelteKit**, are the perfect alternative because they blend so many good qualities into one system.

![Marie Kondo that shit](https://i.redd.it/zoz9jdjga0g21.jpg "Pick SvelteKit")

Here's why it's such a good choice:

- Unrivaled DX
- Small bundle sizes
- Straightforward state management
- Amazing performance and adaptability
- Good and growing community support

## A little background

Svelte came about in 2016 as the brainchild of Richard Harris. The secret sauce is that it is [first and foremost a compiler](https://dev.to/joshnuss/svelte-compiler-under-the-hood-4j20), so, as its name suggests, it can ditch all that extra weight of unused code at runtime. Over the years it has steadily grown in use and support. This summer, Svelte 4 dropped and SvelteKit, the actual framework, hit v1.0. It's been the [most loved framework](https://survey.stackoverflow.co/2023/#section-admired-and-desired-web-frameworks-and-technologies) for the last few years now, and it keeps getting more and more attention for good reason.

## Unrivaled DX

Just *l👀k* at this code comparison. First there's React:

```js
import { useState } from 'react';

export default () => {
  const [a, setA] = useState(1);
  const [b, setB] = useState(2);

  function handleChange (event, setValue) {
    const { value } = event.target;
    setValue(value);
  };

  return (
    <div>
      <input type="number" value={a} onChange={(e) => handleChange(e, setA)} />
      <input type="number" value={b} onChange={(e) => handleChange(e, setB)} />
      <p>{a} + {b} = { parseInt(a) + parseInt(b) } </p>
    </div>
  );
}
```
And this is the same thing, but in Svelte:

```svelte
<script>
  let a = 1;
  let b = 2;
</script>

<input type="number" bind:value={a}>
<input type="number" bind:value={b}>
<p>{a} + {b} = {a + b}</p>
```

**So. Good**. It's explicit, it's direct, it's clear, it's short, it's sweet, it's everything developers want in code. It very simply brings JS into HTML rather than React's less elegant JSX, which takes the opposite approach of inserting HTML into JS. Even CSS can be in the same .svelte file! 

SvelteKit also has quick, easy-to-use transitions, effects, and animations out of the box and has taken inspiration from Next and Nuxt to make building a website a breeze.

## Small bundle sizes

While React will ship over 40 kB of <del>BS</del> JS right out the gate, Svelte will compile all that JS down and only ship what is needed, which is usually around 2 kB 😮. Furthermore, Svelte does away with the Virtual DOM and all its diffing algorithms, instead relying on direct updates to the DOM. This highly optimized method helps speed things along, saving time and money.

## Straightforward state management

I remember in my coding bootcamp when we went over Redux, they said it was hell week and made everybody set this image as our Zoom background:

![Redux sux](https://www.freecodecamp.org/news/content/images/2022/06/2.png "Simple, right?")

We had dispatchers and actions everywhere, and even though we were just updating some credit card info, we had files and files to navigate through just to change a couple numbers. Thankfully, Svelte has simplified state management with built-in, reactive stores and this shorthand for subscribing to them: $. Easy as that. 

[Here](https://joyofcode.xyz/svelte-state-management) is a much more detailed look at how state management is implemented in Svelte, but suffice it to say that it is much, much simpler than in React, Redux, Zustand, or any other system. **And it comes *built-in*** 🤯.

## Amazing performance and adaptability

This chart only looks at memory usage, but other metrics end up being very similar. Plus, this is for Svelte 3, now out of date, and Svelte 5 won't be too far off with even more gains.

[![Green is good](https://blog.logrocket.com/wp-content/uploads/2022/10/svelte-memory-usage-framework-comparison.png "Green is good")](https://blog.logrocket.com/should-you-use-svelte-production/)

With SvelteKit, you can adapt your website for static use or deployment to any number of targets. Within the website, you can opt in or opt out of SSR and CSR to best suit your needs, and you can also prerender pages on different events for even better performance. As mentioned in their docs:

> You can mix and match these options in different areas of your app. For example you could prerender your marketing page for maximum speed, server-render your dynamic pages for SEO and accessibility and turn your admin section into an SPA by rendering it on the client only. This makes SvelteKit very versatile.


## Good and growing community support

While Svelte may not be the most popular, it is the most loved. Its ecosystem of libraries is well-maintained and growing by the day. Most tools you'd want to use already exist, more are being added by the day, and *if* it doesn't exist, you could be the hero that helps everyone else out and creates that library yourself. [Best of Svelte](https://bestofsvelte.com/t/components-and-libraries) does a great job of documenting what all is out there.

![So hot right now](https://www.wahidali.dev/_app/immutable/assets/Svelte-so-hot-dc417e61.webp "Mugatu understands")

## More to come

Svelte 4 was released with the understanding that it's just a prelude to Svelte 5. SvelteKit is now stable. And recently Rich [teased](https://twitter.com/Rich_Harris/status/1688581184018583558) how great Svelte 5 is going to be. The code runs about as close as you can get to vanilla JS, and he hinted that the features are gonna be what sets it even farther apart from the rest of the field. [Others agree.](https://twitter.com/spences10/status/1690712491708252160) Svelte and SvelteKit are now under the good guidance of Vercel, still taking direction from its OG creator, and has lively community support to see it blossom. Sure seems like the right pick.

But who knows, maybe this lengthy praise is all for not and [Astro](https://astro.build/) will kick so much ass that in a month I'll be writing about *it* instead.

And don't even mention [HTMX](https://htmx.org/). Don't. Even.