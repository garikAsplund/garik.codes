---
title: Beginner's mind
date: "2023-10-14"
---

## The OG Singularity

In the beginning there was just one big mystery made up of one infinitesimally small point which contained it all. **The singularity**. No, not *that* singularity.

![The Singularity is near](https://blogs.voanews.com/digital-frontiers/files/2011/03/SingularityIsNear.jpg "Maybe")

But since then, to put it simply, things have evolved. In place of one *thing* we now have protons and neutrons and electrons, atoms, molecules, proteins, amino acids, DNA and RNA, cells, tissues, organisms, superorganisms, ecosystems, planets, solar systems, galaxies, galactic clusters, superclusters, and so on and so forth. **Many things**.

Much like the universe, computers have been increasing in complexity, creating and filling niches at breakneck speeds. First we had analog computers to [tell us when the tides were coming and going](https://hackaday.com/2015/10/08/how-analog-tide-predictors-changed-human-history/). Pretty idyllic. Then we had electro-mechanical computers to help [break the Enigma Code and defeat the Nazis](https://www.iwm.org.uk/history/how-alan-turing-cracked-the-enigma-code#:~:text=Alan%20Turing%20was%20a%20brilliant,Second%20World%20War%20broke%20out.). Pretty horrific. Then we had integrated circuits [take us to the moon](https://wehackthemoon.com/tech/how-integrated-circuits-saved-moon-landing). Pretty futuristic.

Today, however, we have computers in our offices, in our homes, in our fridges, in our cars, in our pockets, in our bodies. Computers allow us to simultaneously shop at Safeway while stuck in traffic, half-listen to Spotify's latest recommended songs, and get mad at Siri as she interrupts our new favorite bop to try and take us back home via the backroads we had no idea existed. Computers do that, but also ***so much more***.

## What does it all mean?

For us devs, what this means is we no longer have to be familiar with punch cards and machine code. Phew, that'd be scary! Instead, we have to deal with layer upon layer of abstractions. These abstractions help simplify how we manipulate computers and code. It gets complicated, though, when the sheer number of abstractions keeps growing and changing, and changing quickly at that.

![Coders be like](https://i.redd.it/x3ty5mnd37g61.jpg "Devs then and now")

In today's world, the newcomer has to know the Holy Trinity of HTML/CSS/JS, how to choose frameworks and pick databases, run both unit and integration tests, containerize their app and deploy it on the edge for maximum uptime and minimal latency, orchestrate said containers with Kubernetes or Docker Swarm, understand the DevOps lifecycle and what a CI/CD pipeline is. All so that when the greenest junior dev makes a change to fix a couple typos they don't bring down the whole company's website.

Granted, I don't think many, or any, are calling for these tools and practices to go away--they have real value! It's just, you know, a lot for newcomers to grasp.

## Too many targets

![Buckle up](https://media.tenor.com/qBfG6bWpBYAAAAAd/tayshia-bachelorette.gif "Tayshia on SWE")

If you want to build an app these days, you have to know your target. Do you want:

    - A website
    - A mobile app
    - A desktop program
    - An embedded computer

You could design a different app for each platform, but that would be painful and costly. For web you have to make sure to design for mobile anyway since they have browsers. It also has to work across all browsers. The mobile ecosystem is split between Android and iOS. Desktops are divided between Windows, Mac, and Linux. Embedded computers you're probably writing in C, maybe C++, possibly Rust now.

Then you need to have all the supporting tools in place. The number of tools is overwhelming, and, for the most part, this is a recent result of good old fashioned competition. Take the case of package managers in JavaScript.

A few years ago you had to use NPM, and as we all know, [Theo's computer maxed out](https://youtu.be/ZIKDJBrk56k?si=HbOcg26X0tZ_XUT7) because of all the Node modules. A couple years ago you were excited about YARN--Yet Another Resource Negotiator--because it was faster, safer, and more reliable! Last year you probably switched to PNPM and were stoked that it had a single store and cached everything, then just referenced that cache with links. So. Speedy. And last month you heard about Bun and questioned everything you knew about life. Can you really install all your dependencies in under half a second?! Kind of--it won't check if the "latest" flag is being honored :( though it's still impressive!

![Run Bun](../Bun.png "Run Bun")

But Bun isn't *just* a package manager. It's also a fast runtime, test runner, and bundler. It tries to simplify the small mess of JavaScript tooling. And unlike Deno, it wants to be a drop in replacement for Node, Jest, Webpack, et al.

However, this is still *adding complexity* to the overall development environment! And there's no end in sight.

There are many "write once, deploy anywhere" tools available, one recent neat addition is [Dioxus](https://dioxuslabs.com/) for Rust. But again, this is adding complexity. Then there's the land of tailored IDEs for languages. [Rust Rover](https://www.jetbrains.com/rust/) just dropped, splitting the Rust community into using an obsolete and maybe open source VSCode extension and a pay-to-play option backed by JetBrains. Examples like this truly are endless.

## The irony of it all

The funny thing is, 99.99% of people will have no idea about any of this mess. No one checking their bank balance is wondering which bundler you used or if the website is written in TypeScript. **No one**.

Sure, they'll complain, "This is slow!" Or they won't notice if it's fast. But they won't be wondering about your bleeding edge tech stack or how secure it is, though maybe they should.

When I thought about transitioning into tech, I chatted with my dad--a retired software architect--about it all. He sketched me a diagram of different areas, like front and back end, along with the languages and tools they used. Immediately I was overwhelmed and scared. Literally just hearing the names and the complexity of it all reminded me that I knew nothing. Hadoop this, jQuery that, Ruby on Rails here, Java there, and JavaScript everywhere. Did I really want to go down this path?

The first few months of learning web dev was, indeed, just learning some made-up name and what it did. What's a Docker? How do you train your K8s? Is Deno pronounced Denno or Deeno or Dino because it has a dinosaur as a mascot? Side question, does anyone ever use it? What's the difference between PocketBase, Supabase, and Firebase?

At the end of the day, all the end user cares about is if something *works*. When they click "post," will their friends see the latest cat content or not?

![The Creation of Catam](https://images.unsplash.com/photo-1545529468-42764ef8c85f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=3546&q=80 "The Creation of Catam")

It really is that simple. As software engineers, we get paid the big bucks to deal with the pains of managing outdated but functioning systems in Fortran and COBOL, migrating codebases from JS to TS for security purposes, and switching servers from Python to Rust because it saves money and time. That is ***our job***.

And yet all of the tools, all of the languages, don't really mean anything to most people. And that's just how it should be: **simple and beautiful**.

![Enso it goes](https://upload.wikimedia.org/wikipedia/commons/6/68/Enso.svg)
