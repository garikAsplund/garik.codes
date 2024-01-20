---
title: JS tools are dropping JS
date: "2024-01-10"
---	

JavaScript recently turned 28 years old and is just as important as ever, but how can you make JavaScript better? By getting rid of the JavaScript, of course. Allow me to explain.

One of the biggest trends in the JavaScript ecosystem right now is to switch to Rust when writing the software that makes JavaScript run. In this video I’ll detail this shift, highlight oxlint, one of the most recent JavaScript tools to adopt Rust under the hood, and explain how big names like Shopify saw their build times go from over an hour to mere seconds when switching to oxlint for linting. Make sure to watch till the end of the video to learn how you, too, can capitalize on the great migration to Rust for JavaScript tooling and start contributing to open source projects that will get you noticed.

Currently we are in the Third Age of JavaScript. During the First Age JavaScript hit the browser and took over the Internet. In the Second Age the developer space came into its own with a package manager in NPM, a runtime with Node, libraries like React and metaframeworks like Next, type safety with TypeScript , test suites like Jest, bundlers such as Webpack, and compilers and transpilers akin to Babel. Today, the Third Age is all about refinement. And most of that refinement is being accomplished with Rust.

Now that the developer tools are known, it’s time to refactor them for speed and safety, which in turn creates better developer and user experiences. Developers get faster builds with fewer headaches and end users get quicker, more secure products. It’s a win-win.

A common theme with today’s rewrites is collapsing layers. Whereas before we had many tools each focusing on one thing, we are now seeing one multi-tool working on all of these tasks. Great examples of this are Deno and Bun. These projects take a runtime, package manager, tester, formatter, linter, and bundler and place them into one binary.

But there’s another Swiss Army knife in the works. The JavaScript Oxidation Compiler, or Oxc project, is “a collection of JavaScript tools written in Rust,” hence the oxidation moniker. They aim to make a Rust-driven parser, linter, formatter, transpiler, minifier, resolver, and VSCode extension designed for the Third Age of JavaScript. They are starting from scratch in order to eke out the most performance wherever possible through better memory allocation and parallelization.

In December 2023 Oxc announced that its linter, oxlint, was generally available for use. They note that it’s currently not a full ESLint replacement and should be used “as an enhancement when ESLint's slowness becomes a bottleneck in your workflow.” Still, the initial results are remarkable.

Oxlint speeds up linting 50-100 times over ESLint, is more accurate and thorough, requires zero config out of the box, has helpful error messages, and is adding more rules every day. It really is the future of JavaScript tooling. And they have great documentation on how you can start contributing to the project today.

In many cases ESLint, its plugins, and dependencies can weigh in at over 100MB and be a pain to configure, taking quite some time to get right. Oxlint is different. It is super small, coming in at only 3MB, and can be run without installing or configuring anything. One of its great advantages, its lack of configuration, can be viewed as a weakness in some cases, though the team acknowledges that and is actively working towards allowing plug-ins on a broader basis.

Even skeptics like Evan You, creator of the framework Vue and the frontend build tool Vite, seem to be convinced. Last year Evan said in a podcast that he was wary of having Rust as the backbone of the JavaScript toolchain because it would be harder to take input from the developer community and hurt interoperability. But now he seems to be changing his tune: “Ran oxlint on the Vue 3 codebase, ~200 rules + ~590 files finished in 50ms 🤯 (30ms re-runs) The performance is absolutely nuts.”

Keep in mind, too, that much of what makes Vite so fast and popular is the adoption of such cutting-edge tooling! Already Evan announced in October that “The cat is out of the bag: we are working on Rolldown, a rust port of Rollup” in order to focus on better performance for Vite’s bundler. So yes, Rust is taking over.

For oxlint one major aspect of their success was starting with an in-house performant parser. Their parser beats other popular Rust parsers like swc by a factor of 2 and Biome by a factor of 3. Further gains were made by utilizing multiple threads whenever possible. And finally, the team at Oxc tunes each linting rule for performance. That means most projects can be linted in under a second, and larger monorepos take just a few seconds. As for Shopify, they saw truly astounding results.

Previously it took 75 minutes to lint their codebase on over 40 workers, but when running oxlint, linting took only 10 seconds. On one worker. That’s essentially 18,000 times faster than before, plus it did a better job at catching problematic code and was easier to understand. It’s no wonder, then, that Shopify DX and creator of Preact, Jason Miller, said “oxlint has been a massive win for us.”

If you’re new to Rust but want to learn more, I have plenty of other videos to help get you up to speed with what makes Rust the best programming language for modernizing the JavaScript ecosystem. Want to learn what “fearless concurrency” is about and why it’s so important? Watch this video I made on how to create threads.

Don’t forget to sign up for your copy of the Rust Cheatsheet and check out my Rust Developer Bootcamp that will set you up to be able to contribute to oxlint and other open source projects built in Rust. Oxlint alone currently has over 10 issues flagged “good first issue,” so start your Rust coding journey today.
