---
title: Code Bloat
date: "2023-08-20"
---

![Feeling bloated?](https://www.ogdenclinic.com/images/blog/Bloat-1.jpg "A bad case of code bloat")

## It starts simple enough

It began with a basic request from my brother to take an experiment he had run a few years back and make it into a website. Previously his research team used [Qualtrics](https://www.qualtrics.com/), a survey company, combined with a large collection of pre-made video files to present a bunch of letters and track participants' reaction times whenever they saw a target letter appear in a different color. It looked something like this:

<video controls width="500">
  <source src="../letters.mp4" type="video/mp4" />
</video>

So I started with the smallest achievable goal possible of making a box with a border, filling it with random letters, and changing one of the letters' color. There were a few design specs taken from [this paper](https://psyarxiv.com/cznh9/), and I was happy that it was easy to get up and running.

But then I reread the paper and the different cases for attentional blink, contingent capture, and surprise-induced blindness and had to implement new functionality. Then I reread the paper again and discovered that there were a few initial conditions that I had missed, so I made sure to include those, too.

## Getting out of hand

The website was looking good! I had the basics covered, so I was confident that I could just sprinkle in a few more features that would be required to wrap it all up into a cohesive research tool to gather data. 

I hooked the site up to Firebase, both for authentication with OAuth and a Realtime Database since it was super easy to use. I tweaked a few conditional renderings in SvelteKit. That's when it dawned on me that I hadn't really thought ahead or planned my codebase accordingly. All of the sudden I was staring at essentially a single file with:

- Auth
- Connection to a database
- Conditional rendering for:
    - Different types of users 
    - Different game state
- The actual experiment with three different flavors of usage:
    - Attentional blink
    - Contingent capture
    - Surprise-induced blindness
- Game over page

## It sneaks up on you

I'd gone from staring at an empty file with only a prompt from my brother, and the next thing I knew I was sorting through over 600 lines of code that had too much functionality, and too many variables, crammed into one location.

![Sneaky sneaky](https://media.tenor.com/PtGEiYSmOQUAAAAd/oh-my-god-where-did-you-come-from-moira.gif "Sneaky sneaky")

As J. B. Rainsberger says:

>Managing complexity is the essence of software development. Break problems into sub-problems. Keep your codebase and your team's focus as small as you can.

So I thought I'd give that a whirl.

## Refactoring

It was clear that I needed to do some retrofitting of my code, but since I had waited to do it, I made my job that much harder. Instead of thinking ahead, I now had to think backwards and change already working code. Inevitably this leads to frustration as you go from a functioning app to a broken app.

![Trouble coming](https://user-images.githubusercontent.com/24452340/172385080-4f37f8e1-98bb-434b-bb85-9d377551c75c.png "#Truth")

I started with moving some of the smaller sections of the website to separate components. Easy enough. I also utilized a store to share state between the couple of different areas of my app. I was happy with how refactoring was going.

Then I thought I should tackle the main code and separate it out into its own component and store. **Modularity! Maintainability!** I was *software engineering*.

It also hit me that I wasn't following best practices because I was getting deep into no man's land with all this refactoring that might be all for not. I panicked. How many Ctrl+Zs can you do?? How do you go back to your previous commit?

Fortunately it wasn't that bad.

```js
git checkout -b testing123
```

And then a quick:

```js
git checkout main
```

Voila! Back to the main branch without the crazy complicated mess of trying out some code alterations that may or man not work. But it got me thinking.

![The trouble is](https://media.tenor.com/XvpdInd9ia4AAAAd/refactoring-code-cat.gif "Maybe maybe maybe")

## Is it worth it?

The toughest thing is, I'm not sure whether to go down the refactoring road even further to make the code somewhat more modular and maybe more maintainable, or to let it wither on the vine. As it stands, this project is super small and only a couple of people will ever be looking at it. Do I spend my time pursuing something that doesn't really add much to the project and could be a dead end, or do I just leave it all a bit messy?

[Good code is a love letter to the next developer who will maintain it](https://addyosmani.com/blog/good-code/). I want to provide something that is easy to navigate through and make alterations, but I'm not sure if that's with a medium-sized file that does many things with good labeling, or if it is to compartmentalize it all into smaller files, do a little more importing here, some exporting there, do some storing elsewhere, and hope that for non-coders it's not too much to handle. 

If the project were bigger, it'd be an easy decision. Break. It. Down.

For now, I'll just wait and hopefully next time I can better judge how to split things up in advance. Maybe.

![Building be like](https://i.pinimg.com/originals/9a/a7/24/9aa7241c91aa10636577ef1d1f11a25a.png "Building be like")