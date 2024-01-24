---
title: Contributing to open source 
date: "2024-01-23"
---

A little while ago I had my [first successful pull request](https://github.com/mskocik/svelty-picker/pull/147/commits/e967c10fbb2a2c8352eb90551a363b97a29d533e) merged into an open source project. It was silly how small of a contribution it was--all I did was help clarify a variable in a date picker. Basically, [JavaScript is weird](https://github.com/denysdovhan/wtfjs?tab=readme-ov-file#what-the-fck-javascript), and this project just needed to take that into account to advance the calendar page properly.

This was the whole change:

```js
    newActiveDate.getDate() > 28 
        ? newActiveDate.setDate(newActiveDate.getDate() - 3)
        : newActiveDate;
```

## Let's be real

That contribution is not gonna land me a job. But I'm still happy I did it. I was using the date picker for a project and ran into a problem, so I dug a little deeper and saw that someone had already opened an issue on GitHub. Then I forked and cloned the repo, scrolled through and found out what was wrong rather quickly.

Not everyone is up for that small distraction. But *someone* is--that's the whole point of open source.

![Don't be him](https://miro.medium.com/v2/resize:fit:1018/1*p8p2T0cg5pFkxXpVogrXaw.jpeg "Chad")

## Diluting the space

But that point is getting lost.

[Theo recently posted](https://www.youtube.com/watch?v=5nY_cy8zcO4) why you shouldn't contribute to open source. It's not a blanket statement that no one should contribute. Rather, it's a complaint lodged at

- Hackathons improperly incentivizing contributions so that they end up being paltry and annoying
- People naively thinking contributing anything at all will land them a job

The last thing these pull requests are is helpful.

And I agree. At my bootcamp our big final project was to hop on with a small team and fix or enhance open source projects. The thing is, though, all of these projects came from [Open Source Labs](https://www.youtube.com/watch?v=5nY_cy8zcO4)--some kind of weird shell company to disguise the fact that bootcamp attendees are writing all the code.

![OSLabs](https://habrastorage.org/getpro/habr/upload_files/0f0/3cc/0e7/0f03cc0e756167009b82bd3c5fdcdb4a.jpg "For developers, developers, developers")

There are some benefits to this, and also a bunch of problems.

## Smart, sneaky

The idea is to get green developers some real world experience and pad their resumes. It's a relatively safe space to do so because a lot of the projects are unheard of or not in use. It's low stakes but feels like the real deal. Each developer has to go through the motions to contribute to the project.

Every now and again, a new idea is pitched and picked up that has some modest impact. The largest projects have about 2.5k stars and are largely prototyping tools like [OverVue](https://www.overvue.org/).

It's worth mentioning that the amount of research teams do in preparation for picking a project is actually quite high. I'll grant, too, that it does teach new developers the art of onboarding.

## Dishonest, damaging

On the flip side, the bulk of these projects are broken and don't really help anyone. If asked in an interview what my time working on [Quell](https://www.quell.dev/) was about, I'd struggle to come up with a meaningful answer. We inherited a broken GraphQL cache for servers and clients similar to [Apollo](https://www.apollographql.com/), our advantage being we were lighter weight. We did our best to patch it up so that it actually did what it said it did. That's not nothing.

Still, it feels like we're putting the cart before the horse here. Instead of making websites or apps that utilize open source tools and coming across issues as they arise, the bootcamp automatically says you need to contribute to on open source project. Worse, that's still their stance even if the open source project is rarely used and keeps breaking since every 6 weeks it's being tweaked by a bunch of people who have very little experience coding.

The biggest constraint here is time. Bootcamps need to move people through, like yesterday. So they can't afford the luxury of having developers work on a project for a while and maybe, maybe not come across true problems in some dependent library.

## A better way

So what to do? Well, the best thing is to read [GitHub's "How to Contribute" guide](https://opensource.guide/how-to-contribute/) and familiarize yourself with it. The gist of it all is to

- Use tools organically and fix issues that affect your projects
  - If you don't fix it, [at least mention it in an issue](https://github.com/skeletonlabs/skeleton/issues/2297)
- Research a project and isolate issues that you can tackle

That's it. **Don't spam. Don't nitpick. Don't mess things up.**

![Please help](https://i.pinimg.com/736x/9e/77/4a/9e774a4d191b645966234b94f33a45c8.jpg "Be a Buddy")
