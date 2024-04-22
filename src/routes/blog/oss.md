---
title: "Open Source Summit 2024"
date: "2024-04-21"
---

## Here's what's up

![Newsflash](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdDNkczNpenQ1bHdyZzc5bHpib3M3N3lnNmJjbnc5Mm80YXM5amdxcCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/MPut2RK0Ue3sPFBM3s/giphy.gif "Newsflash")

Last week I spent a few days at The Linux Foundation's [Open Source Summit](https://events.linuxfoundation.org/open-source-summit-north-america/) held at the Seattle Convention Center. These were the things everyone was talking about:

- Security and trust in a post xz world
- Wasm, Wasm everywhere
- The right to fork

## Security versus trust

Maybe you heard the whole internet was [almost brought down by a backdoor attack](https://www.synopsys.com/blogs/software-security/xz-utils-backdoor-supply-chain-attack.html). This was a scare for many people, and the open source community was discussing how to mitigate disasters like this.

Everyone basically agreed that *security* is not the same as *trust*, and there needs to be better mechanisms in place to uphold trust. The trouble is, there aren't agreed upon ways of doing that.

So, despite not having any answers, at least there was a healthy ongoing discussion about what trust looks like in this space.

![Do you trust me?](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExamY0Y21peXU1MGIzcGh3eHNhcW5jN3ZlbzFhZnZzdzlmN251YTI1aCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/voF2A48B0XQje/giphy.gif "Do you trust me?")

## Wasm for the win

Sure, I've heard of Wasm. It's a cool idea--run any code in the browser, not *just* JavaScript. But that idea is [floundering](https://www.youtube.com/watch?v=fbd0MEWnPkE).

Little did I know that Wasm is exploding in serverless contexts. Like, it's a really big deal.

[![Wasm is a big deal](../docker.png "Wasm is a big deal")](https://twitter.com/solomonstre/status/1111004913222324225?lang=en)

Long story short, Wasm enables **super small, super secure, super fast** containers. It's as if a bunch of people designed the perfect container from the ground up. But they didn't. It was a happy accident.

And that's not all! Wasm is also able to run on any platform without configuration. Plus, with components, you can mix and match languages and libraries in endless ways to save you from headaches.

![Wasm everywhere](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZW93ODRvdXFreTVka2pnN3ViOHhrdXY4MmZraDEzZjV3cG95dzcxMiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/SbtWGvMSmJIaV8faS8/giphy.gif "Wasm everywhere")

As the [Cloud Native Computing Foundation](https://www.cncf.io/) says:

 >Containers are the new normal, and WebAssembly is the future.

## Right to Fork

Not that long ago [Redis](https://redis.com/)--the biggest database for caching--made a huge, surprise move and changed their license. Basically it's no longer open source, and that pissed a bunch of people off.

Fortunately, in OSS there is the ["right to fork."](https://opensource.stackexchange.com/questions/345/what-does-the-right-to-fork-mean#:~:text=The%20right%20to%20fork%20refers,right%20to%20redistribute%20modified%20copies.) Anyone who is upset with a project can fork it and do what *they* want with it.

![Fork yeah](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdGp1amQ1MmwwcjV4eDRsNDJldTgwOW81ZDc3cjU1cW9uMzhkb3BzNCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/l41m4JwuW9gaOwGcg/giphy.gif "Fork yeah")

That's exactly what happened with Redis. In a matter of weeks key maintainers and valued contributors--I'm sorry, I couldn't resist--forked Redis and released a stable open source version called [Valkey](https://valkey.io/).

Industry is behind the move. People are behind the move. It's cool to see so many people hop on a project this fast and keep open source alive and well.
