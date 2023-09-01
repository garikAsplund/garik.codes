---
title: Why not Python?
date: "2023-08-13"
---

![Python. Gross.](https://media.tenor.com/E4F_uLU34UsAAAAC/why-did-it-have-to-be-snakes-indiana-jones.gif "Indy knows")

**Python**. It very well could be the [most used](https://pypl.github.io/PYPL.html) programming language out there. It's easy to see why:

- [It's beginner friendly](https://wiki.python.org/moin/BeginnersGuide/NonProgrammers)
- [It has a vast amount of libraries](https://www.interviewbit.com/blog/python-libraries/#:~:text=With%20more%20than%20137%2C000%20libraries,data%20manipulation%2C%20and%20many%20more.)
- [It's named after Monty Python](https://docs.python.org/3.8/tutorial/inputoutput.html#the-string-format-method)
- [**Other people use it**](https://www.tiobe.com/tiobe-index/)

I've bolded that last item because it's likely the real reason that Python is popular. That might seem like a [Yogi-ism](https://yogiberramuseum.org/about-yogi/yogisms/), but it's true.

## The wrong tool for the job

Python is used most widely in data, analytics, and machine learning, with a lot of the work including image manipulation and data visualizations. All of these tasks deal with massive data sets and file sizes, meaning the code is crunching numbers all day, all night. So, Python, as a language, should be mad fast and efficient and secure, right? Right!

It **should** be, but most definitely *isn't*.

![Slow](../python2.png "Oh nooooo")
![Fast](../python1.png "Oh yeaaaaaah")

# 🐍 == 🐌

Here's the rub. Python is the **worst** choice for doing what it does. Of note, Python is

- One of the [slowest programming languages](https://github.com/niklas-heer/speed-comparison/blob/master/README.md) out there
- Insanely [memory intensive](https://stackoverflow.com/questions/49031058/optimizing-memory-usage-pandas-python) and [power](https://www.efinancialcareers.com/news/2023/06/which-programming-language-uses-the-most-energy) [hungry](https://thenextweb.com/news/python-progamming-language-energy-analysis)
- [Vulnerable](https://thehackernews.com/2022/09/15-year-old-unpatched-python.html) to [attack](https://thenewstack.io/compiled-python-code-used-in-a-new-pypi-attack/)
- Susceptible to [random runtime errors](https://medium.com/metabob/chasing-memory-spikes-and-leaks-in-python-172ae99290d3)

Each one of these issues, *by itself*, is reason enough to look for a different paradigm. Put another way, **Python is sluggish, selfish, poor at its job, and let's the bad guys in**.

![GOB Knows](https://64.media.tumblr.com/84c8ce7dd9d89bfcca79788f763cb97e/tumblr_mngx21FyhC1qa8jwfo1_500.gifv "Cock-a-caw")

## Too little too late

The thing is, the Python community kind of knows these shortcomings. Kind of. In 2020, none other than Microsoft [lured](https://www.zdnet.com/article/guido-van-rossum-the-python-languages-founder-joins-microsoft/) the creator of Python, Guido van Rossum, out of retirement to head up a team to revamp the language with the goal of making it twice as fast, or still 5-50x slower than C, C++, or Rust 🤦. That's pretty pathetic.

The 3.11 release of Python gained 25% over 3.10. Whelp. That took a team at Microsoft *years* to accomplish. There are already much better choices out there that are safe as safe can be and run on bare metal blazingly fast. Plus, these competitors adhere to zero-cost abstractions and backwards compatibility, which we'll get to in a minute. **The war is already over, guys**.

What's more, Guido previously worked at Dropbox and was tasked to "wrangle four million lines of Python code." Python is supposed to be cool because it's Zen. It even has a poem you can import called The Zen of Python:

```python title="Say hello to Shiki highlighting"
>>> import this

The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

But it's also possible that being one of the only kids on the block to ditch braces actually leads to difficulty programming in other languages or creates confusion. Being "Pythonic" is awesome, until it's not. At times it's childish.

```python
>>> from __future__ import braces 

SyntaxError: not a chance
```

And other times being Pythonic also borders on being moronic. Martin Fowler knows:

> Any fool can write code that a computer can understand. Good programmers write code that humans can understand.

The problem is that Python code tends to be less extensible than other code. So not only is it slow to run on machines, it's slow in the hands of humans, too, which is very costly. Take [this example](https://www.zdnet.com/article/python-programming-language-creator-retires-saying-its-been-an-amazing-ride/) from Dropbox:

> When the company grew, new engineers could not understand the clever but 'short and cryptic' code written by and for earlier developers.

And, for being so Zen, Python sure [botched](https://news.ycombinator.com/item?id=15708136) the [transition](https://www.wired.com/story/think-app-updates-suck-try-upgrading-programming-language/) from version 2 to 3. Like, [majorly](https://stackoverflow.blog/2019/11/14/why-is-the-migration-to-python-3-taking-so-long/). Dropbox, which had Guido himself to guide the process, took over 3 years to migrate from 2 to 3, and wasn't done by the time he retired. Moreover, the Dropbox team basically said, "F this," and [switched their sync engine to Rust](https://dropbox.tech/infrastructure/rewriting-the-heart-of-our-sync-engine) with amazing gains across the board, calling it a "force multiplier for our team, and betting on Rust was one of the best decisions we made." Ouch.

[Here's an account](https://www.activestate.com/blog/python-2-to-3-migr) of a developer's experience in migrating over from Python 2 to 3. Let this sink in:

> When I prepared for my migration, I read a lot about Python 3. I was surprised to find that it has been in development since 2005! The first release was way back in 2008. Ever since then the Python community has been pushing for developers to make the jump. However, after an unsuccessful deadline in 2016, the community decided to do a hard stop in 2020.

It took over a decade with breaking changes to sever ties to Python 2, and yet, somehow, many people and companies are still using Python 2 despite its vulnerabilities.

## Allegory of the battle of the bears

![Polars vs. pandas](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*2EHqvZVV4qNjRqrHiBK9-A.png "There's a new bear in town")

For data manipulation, the go-to option is pandas. It's been the choice for some time, but recently a new bear arrived on the scene: Polars. Polars is written in Rust, so it all but takes care of every single shortcoming that Python, and by way of extension, pandas has. It's not a fair fight, really.

Read more about the breakdown [here](https://medium.com/cuenex/pandas-2-0-vs-polars-the-ultimate-battle-a378eb75d6d1), [here](https://betterprogramming.pub/data-duel-pandas-2-0-and-polars-0-17-7-battle-for-supremacy-in-speed-and-syntax-87f062995550), [here](https://studioterabyte.nl/en/blog/polars-vs-pandas) and [here](https://www.makeuseof.com/pandas-vs-polars-which-is-better/), but this is the key takeaway:

> While Pandas can take minutes of time to simply sort the data frame, complex sorting functions can be evaluated in not more than 15 seconds in polars.

Here's what it looks like in graph form:

![pandas vs. Polars](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*cRKPevCMbpaBiR4rFLetPQ.png "Rust FTW")

Add in that pandas, much like the Python team of yesteryear, is [repeating the mistake](https://www.infoworld.com/article/3513440/pandas-10-brings-big-breaking-changes.html) of not taking [backwards compatibility](https://stackoverflow.com/questions/75956209/dataframe-object-has-no-attribute-append) seriously. Big bummer.

> Long time pandas user but changes like this are why polars is becoming more popular i guess

## Maybe Mojo 🔥

The most promising recent development is [Mojo](https://docs.modular.com/mojo/why-mojo.html). Chris Lattner, who also spearheaded Swift, has been influenced by Rust and &borrowed--[get it??](https://betterprogramming.pub/the-magic-of-borrow-checkers-in-rust-238a2a97bff2)--heavily from the 🦀🦀 to gift the world with Mojo. Some benchmarks show that Mojo is **35,000x faster** than Python, and, as a **superset of Python**, you don't have to worry too much about throwing away your old code, doing a whole rewrite, or training a team the ins and outs of Rust. It's still extremely new and untested--like, it doesn't even have classes yet--but it sure seems like *this* is where people should be focusing moving forward.

> The Mojo language has lofty goals: we want full compatibility with the Python ecosystem, we want predictable low-level performance and low-level control, and we need the ability to deploy subsets of code to accelerators. Additionally, we don’t want to create a fragmented software ecosystem—we don’t want Python users who adopt Mojo to draw comparisons to the painful migration from Python 2 to 3. These are no small goals!

Stay tuned. It'd be great, too, if this team also solved Python's package management issues. One can dream.

[![Too true](https://imgs.xkcd.com/comics/python_environment_2x.png)](https://xkcd.com/1987/)

## Sayonara, snake

So why deal with all this hassle? Well, **don't**. The path forward is pretty clear. For decades Python has risen in popularity, and despite this, the changes to the language and its ecosystem of libraries show that improvements are still wanting in major ways, and what improvements there are come with heavy costs.

The world of machine learning, IOT, and AGI is not far off, and that world will only require *more* timeliness, *more* safety and security, and *more* efficient use of resources. These are things that Python cannot and will not deliver. Python is great for hobbyists and kids who are just getting into programming via [RaspberryPi](https://www.raspberrypi.com/), but it should not be the language of choice as we are steadily [handing over the reigns](https://builtin.com/artificial-intelligence/artificial-intelligence-future) to computers.
