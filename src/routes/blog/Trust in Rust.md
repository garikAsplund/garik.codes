---
title: Trust in Rust
date: "2023-08-30"
---

![Memetics](https://external-preview.redd.it/IAMB6TV2YcGBo67tBJGJLpE9T2HnPTR_acYEe4uJrG8.png?auto=webp&s=d8f1ca2c748425d0c6a81f5de20c9297739e56a1 "Rust everywhere")

No, don't do that. Rust is a peculiar language with a steep learning curve that is really great in certain situations. **But which situations?**

Since Rust is a systems programming language, the obvious place to implement it is operating systems and hardware. I mean, the guy who created the language, Graydon Hoare, started the project while he was at Mozilla because [the elevator in his apartment building wasn't working](https://www.technologyreview.com/2023/02/14/1067869/rust-worlds-fastest-growing-programming-language/). No joke. So, with that as its starting point, and after years of development, the major advantages of Rust are that it is

    - As fast as C
    - Memory safe
    - Super reliable
    - Won't crash your elevator

Add in the fact that the compiler throws errors that are actually ***helpful*** and you have a pretty good situation going.

It took a while to get Rust to a stable release accompanied by a vibrant ecosystem of well-managed libraries, but now that those are in place, Rust is spreading like wildfire. Or like the rust fungus in the wind. [Or like crabs after the first rain](https://parksaustralia.gov.au/christmas/discover/highlights/red-crab-migration/#:~:text=When%20does%20the%20red%20crab%20migration%20occur%3F&text=The%20migration%20starts%20with%20the,ocean%20to%20mate%20and%20spawn.). Or something.

## Who is adopting Rust?

![Boromir knows](https://raw.githubusercontent.com/rochacbruno/rust_memes/master/img/notsimply.jpg "Boromir knows")

For starters, let's just get the big names out of the way:

    - Microsoft
    - Google
    - Amazon
    - Facebook

Why is it being used in these companies? All of them have deep pockets, so they can afford to take on lengthy, difficult rewrites. But the real reason is that they have to.

Microsoft Azure's CTO, Mark Russinovich, had this to say:

[![Rust at Microsoft](../Rust_Tweet.png)](https://twitter.com/markrussinovich/status/1571995117233504257?lang=en)

At Google's behest, Linux--the open source OS of choice for Android, not to mention 100% of the top 500 supercomputers, and the majority of servers--is slowly introducing Rust into its kernel. This is **huge**. Never before has Linux offloaded any compute away from C. *Ever*. Until now. Once, in the 90s, they toyed with using C++, but after two weeks [abandoned ship](https://en.wikipedia.org/wiki/Rust_for_Linux#cite_ref-1). Linus Torvalds also went on a [mini tirade](http://harmful.cat-v.org/software/c++/linus) about how bad C++ is when he was inventing Git. Oh yeah, you forgot he created **Linux *and* Git**??

In his own words:

> In fact, in Linux we did try C++ once already, back in 1992.
>
> It sucks. Trust me - writing kernel code in C++ is a BLOODY STUPID IDEA.

So, Rust in the Linux kernel! Big deal! Sure, this is a slow start, but a major start just the same.

![Linux world headquarters](https://i.redd.it/6gm50gpd5y761.png "The man. The myth. The legend.")

Even though Linus is known for his temper, we should also remember him for [this gem of a quote](https://youtu.be/o8NPllzkFhE?si=JlnTHf5o1xNfA-ST&t=126) about his preferred workspace:

> I want to hear the cat purring, not the sounds of the fans in the computer. ฅ^•ﻌ•^ฅ

But back to the topic at hand. Last year [Facebook said](https://engineering.fb.com/2022/07/27/developer-tools/programming-languages-endorsed-for-server-side-use-at-meta/) that Rust is the only option when it comes to writing new CLI programs, and went on to add:

> The number of projects using Rust inside Meta has increased at an accelerated rate. We’re excited to see Rust added to this list of server-side supported languages, giving our engineers more tools, flexibility, and support for their work.

At Amazon they have had great success rewriting Firecracker, Simple Storage Service (S3), Elastic Compute Cloud (EC2), CloudFront, Route 53, Bottlerocket, and AWS Nitro SystemADD in Rust. So, yeah, [Amazon loves Rust](https://aws.amazon.com/blogs/opensource/why-aws-loves-rust-and-how-wed-like-to-help/).  

AWS, the world's top Internet infrastructure provider, says:

> One of the most exciting things about the Rust programming language is that it makes infrastructure incredibly boring.

Dropbox adopted Rust even when they had the Benevolent Dictator For Life Guido van Rossum on their team migrating their codebase to Python 3. Seriously. Discord started using Rust and improved their average response time 10x and their worst latencies 100x. Figma uses it. The list goes on and on.

![Big improvements](https://d2908q01vomqb2.cloudfront.net/ca3512f4dfa95a03169c5a670a4c91a19b3077b4/2022/02/09/sust-rust-9.png "Oh, I see")

## Startups

This is great! Rust is being taken in by the MAANG gang and many mid-majors to speed things up, save money, save the environment, save engineers and customers the hassles associated with lax security, and everyone should code everything in Rust everywhere all the time forever and ever. Amen.

![Rewrite it in Rust](https://i.redd.it/9oez8zkg1qc01.png "Rust everywhere")

Well, not so fast. There are some key areas where Rust doesn't really make sense.

Recently I applied to a startup that says they want to integrate ML and AI with healthcare. They're based in NY and seem like they mean business. But here's the thing, they want a back end built with Flask, and that is a terrible idea. Maybe that was okay like a decade ago, but we know better now. Flask will be slow and have security vulnerabilities. Servers will be expensive to run and will probably crash for no reason at random intervals. The alternative is to have a back end written in Rust because it offers **speed, security, and stability**.

Because I was trained as an economist, I see tradeoffs everywhere. In this situation, the tradeoff is between having a team that can write front end and back end code in the same language versus a team that is bilingual, and thus bifurcated. The advantage of sticking to one language in a codebase makes development easier and faster, the code more maintainable and extensible, yadda yadda yadda.

![Yadda yadda yadda](https://media.tenor.com/ZeGdcWK2APYAAAAC/seinfeld-blah.gif)

It's the same reason why you see websites use React up front and Node in back--it's all just JavaScript. JavaScript everywhere! Pay one dev to do it all? Easy.

Yet, this startup's project seems to be pretty large, and there are separate roles advertised for front end, back end, full stack, and data scientist. The extra time it takes to develop a back end in Rust will surely be worth it because it will be

    - Faster executing requests
    - Cheaper to run servers
    - Highly secure handling personal information
    - More stable and reliable
    - Easier to iterate upon and maintain

Yes, keep the ML/AI code written in Python because that's probably too much of a task to switch over to Rust. Perhaps in the future they could adopt Mojo and see gains across the board, but for now the best move would be to pair the easy Python data crunching with the speed and security of a Rust back end. Even Gilfoyle, who doesn't trust anyone, probably trusts Rust on the back end.

![Is it safe?](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExb3Jvcm94M2UzdjFsNGJ0NjdidjZ3cGI3am9uZWV2a3VnMGpnYWw2MiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/l46Cgwa9YZNNrEQla/giphy.gif "Head of security")

## Wrapping up

Rust should not be used everywhere, though people who have drank the Kool-Aid may try to convince you otherwise. It's definitely not good if you want to test something out real quick, make a bunch of changes to your codebase in a short period of time, hire a team at the drop of a hat, or do something that doesn't require performance or protection.

**For those situations, stick to JavaScript or Python**.

Outside of that, though, it *does* make sense to use Rust for many things. Need a secure server that handles millions of requests a day, has zero downtime, and saves on energy use? Rust can help with that. Need to have a car that isn't hackable? Rust can help with that. Need to rewrite your OS and limit vulnerabilities? Rust can help with that.

![Ancient crustaceans](https://i.imgflip.com/1sk8j6.jpg "Rust, in a nut shell")
