---
title: Beginner's Mind
date: "2023-09-06"
---
This post is a response and riff on [ThePrimeagen's video](https://www.youtube.com/watch?v=jL88IAxoYOk) about why he feels bad for n00bs in the software game today.

**TL;DR it's a complex world out there and it's getting more complicated all the time**.

![The 5 stages](https://assets-global.website-files.com/5f3c19f18169b62a0d0bf387/60d33be89c10a5b2f1d5dec6_wEUE9CgYOhBCLN7l5mZ3-DkRM7Pi4wVnfVhE0bRBsJsh-cb1g0bbi8S2oRDj5ssjDwo7cqi4T9PDuPrT6zIV1LxX2GX4fyxx8G8XnNbGUFvM5Q1m-lqGiQqi0c8BfCeVIztTRIt5.png "This is wrong?!")

## The OG Singularity

In the beginning there was just one big mystery made up of one infinitesimally small point which contained it all. **The singularity**. No, not *that* singularity.

![The Singularity is near](https://blogs.voanews.com/digital-frontiers/files/2011/03/SingularityIsNear.jpg "Maybe")

But since then, to put it simply, things have evolved. In place of one *thing* we now have protons and neutrons and electrons, atoms, molecules, proteins, amino acids, DNA and RNA, cells, tissues, organisms, superorganisms, ecosystems, planets, solar systems, galaxies, galactic clusters, superclusters, and so on and so forth. **Many things**.

Much like the universe, computers have been increasing in complexity, creating and filling niches at breakneck speeds. First we had analog computers to tell us when the tides were coming and going. Pretty idyllic. Then we had electro-mechanical computers to help break the Enigma Code and defeat the Nazis. Pretty horrific. Then we had integrated circuits take us to the moon. Pretty futuristic.

Today, however, we have computers in our offices, in our homes, in our fridges, in our cars, in our pockets, in our bodies. Computers allow us to simultaneously shop at Safeway while stuck in traffic, half-listen to Spotify's latest recommended songs, and get mad at Siri as she interrupts our new favorite bop to try and take us back home via the backroads we had no idea existed. Computers do that, but also ***so much more***.

## What does it all mean?

For us devs, what this means is we no longer have to be familiar with punch cards and machine code. Phew, that'd be scary! Instead, we have to deal with layer upon layer of abstractions. For the most part, these abstractions help simplify how we manipulate computers and code. It gets complicated, though, when the sheer number of abstractions keeps growing and changing, and changing quickly at that.

In today's world, the newcomer has to know the Holy Trinity of HTML/CSS/JS, how to choose frameworks and pick databases, run both unit and integration tests, containerize their app and deploy it on the edge for maximum uptime and minimal latency, orchestrate said containers with Kubernetes or Docker Swarm, understand the DevOps lifecycle and what a CI/CD pipeline is. All so that when the greenest junior dev makes a change to fix a couple typos they don't bring down the whole company's website.

## Too many targets

![Buckle up](https://media.tenor.com/qBfG6bWpBYAAAAAd/tayshia-bachelorette.gif "Tayshia on SWE")

If you want to build an app these days, you have to know your target. Do you want:
    
    - A web app?
    - A mobile app?
    - A desktop app?
    - Some of the apps?
    - All of the apps?

*actual app*, then you need to target both Android and iOS--so now you're writing in Kotlin or Dart for Google products and Swift for Apple products. Or maybe you want a desktop program, so you could use Electron to transpose a React-like project from the web. Then you have people trying to simplify all of this so you can just write once and deploy everywhere. In Rust there's a neat project, [Dioxus](https://dioxuslabs.com/]), doing just that. But, this is still *adding complexity* to the overall development environment! And there's no end in sight.

![He has a point](https://devs.lol/uploads/2021/11/meme-dev-humor-every-day-there-is-a-new-javascript-framework-86.jpg)

## Carrying technical debt
    
    - Cobal and fortran
    - React
    - Redisigning JS-- tale of JSON guy
    - WASM
    - C, C++, C#
    - Rust, Lobster
    - Zig, etc etc etc

## The irony of it all

![Coders be like](https://i.redd.it/x3ty5mnd37g61.jpg "Devs then and now")

The funny thing is, 99.99% of people will have no idea about any of this mess. When I thought about transitioning into tech, I chatted with my dad--a retired software architect--about it all. He sketched me a diagram of different areas, like front and back end, along with the languages and tools they used. Immediately I was overwhelmed and scared. Literally just hearing the names and the complexity of it all reminded me that I knew nothing. Hadoop this, 

At the end of the day, all the end user cares about is if something works. Can you send cat videos or not?

## coding landscape

    - build tools
        - Webpack
        - Rollup
        - Vite
    - package manager
        - JS
            - npm
            - yarn
            - pnpm
        - Python
            - pip
            - pipenv
            - Poetry
            - Conda / Anaconda / Miniconda
    - frameworks
        - React
            - Next
        - Angular
        - Vue
            - Nuxt
        - Svelte
            - SvelteKit
        - Solid
            - SolidStart
    - languages
        - Front end
            - HTML
            - CSS
            - JS
            - WASM
        - Back end
            - Node
            - Ruby
            - PHP
            - Python
        - Blurry
        - CSS
            - Vanilla
            - Tailwind
            - Bootstrap
            - 
    - runtime
        - Node
        - Deno
        - Bun
    - cloud services
        - Amazon Web Services
        - Google Cloud Platform
        - Microsoft Azure
        - Alibaba Cloud
        - Oracle
        - IBM Cloud
    - targets
        - Web
        - Mobile
        - Desktop
        - Embedded

![Enso it goes](https://upload.wikimedia.org/wikipedia/commons/6/68/Enso.svg)
