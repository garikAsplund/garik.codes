---
title: Prettier just got faster
date: "2024-01-22"
---

## Money talks

Let's face it, everyone uses Prettier for formatting JavaScript. There’s just one thing--Prettier is stuck in 2017. Or at least it had been until they [set a bounty](https://console.algora.io/challenges/prettier) and got a quick Rust makeover.

Rewrites in Rust are infamous for requiring large teams, with deep pockets, long amounts of time to finish. So how was Prettier made faster in a matter of weeks by only a handful of people?

![Rewrites in Rust](https://media.tenor.com/Ok8kj4G5YRcAAAAe/dsmp.png "Seems about right")

## Backstory

It’s hard to believe, but Prettier was released only 7 years ago. Originally written in JavaScript, for JavaScript, Prettier solved a problem that had plagued teams of developers since the beginning of time: tabs or spaces, and if spaces, how many spaces?

![Tabs vs spaces](https://i.gifer.com/6VdJ.gif "Uh oh")

Can you imagine a world without code formatters? No, you can’t. There’s no going back. There’s only going forward, which for Prettier meant dropping JavaScript and turning to Rust to solve issues involving speed and safety. No surprise there, really.

![Slow isn't sexy](https://s.yimg.com/ny/api/res/1.2/2Ilaz0re4n6y.X3O62vnLA--/YXBwaWQ9aGlnaGxhbmRlcjt3PTY0MDtoPTQyNw--/https://s.yimg.com/os/creatr-uploaded-images/2020-09/261ad470-fe76-11ea-ae7f-3f1af8ee7875 "The pain")

It can take 10-12 seconds for Prettier to format large codebases. That might not seem like long, but in the computer world that is an eternity. Not only that, there were many times when Prettier would run into issues like “undefined is not a function.” Good luck solving that one!

![The horror](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSmcQfQ-XWPLqZ0R8gdJ5YoAgZifF91tycjiA&usqp=CAU "The horror")

## Just ask for help

Which is why on November 9, 2023, the Prettier team posted a $10k bounty “for any project written in Rust that would pass 95% of the Prettier test suite.” Then the CEO of Vercel, Guillermo Rauch, personally matched it. All told, there was $25k waiting for whoever cracked the code.

And after only 3 weeks, someone claimed the prize. Well, someones, really. Here’s how the 9-person team at [Biome](https://biomejs.dev/) did it.

## Get a massive headstart

![You call the shots](https://i.imgflip.com/28r2rs.jpg "Biome to the races")

First, they already been working on their project for some time. When the bounty was announced, they were at 85% compatibility with Prettier tests because they were rewriting in Rust before everyone else.

Still, closing a 10% gap can be daunting. So the team welcomed new contributors and [they hopped on GitHub](https://github.com/biomejs/biome/issues/720) to communicate who would solve what issue. They found redundancies, bugs, and much more.

The result? Formatting that is more accurate and 25 times faster than Prettier! Plus it also outperforms ESLint for catching bugs in your code since it lints 15 times faster.

## #Trending

Isn’t it amazing how a little cash and a public spotlight can turn things around quickly? Think of how much the developer experience can be improved by similar projects. Already we’ve seen JS runtimes and bundlers get complete redos in Rust. We are squarely in the [Third Age of JavaScript](https://www.swyx.io/js-third-age), which I'll write more about soon.

What once was good enough just got better, thanks to Prettier’s humility, Biome’s teamwork, and Rust being Rust.
