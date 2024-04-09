+++
title = "GLOW: releasing a game on steam!"
date = 2024-04-09

[extra]
modified = 2024-04-09
tags = ["game", "project"]
authorURL = "https://frankhampusweslien.com/"
author = "Frank Hampus Weslien"
twitterAuthorID = "@HampusFrank"
description = "I'm about to release a game on steam!"
+++

Hello, people of the internet!

I'm in the midest of releasing a game on Steam called [GLOW](https://store.steampowered.com/app/2896110/GLOW/). Here is the description directly from the Steam page:

> "_GLOW is an addictive physics-based arcade game that will challenge you to your limits. Push, dodge, and trick enemies while collecting points as the difficulty increases._"

I know what you are thinking: what is the tech stack? Well, I'm glad you asked! The game is built using the [Bevy](https://bevyengine.org/) game engine and written in Rust!

Here are some of the current pros and cons of using bevy:

- Pros:
  - Rust
  - Fast
  - Static typing
  - Free
  - Open-source
- Cons:
  - Documentation
- The community is small but very helpful
- Tutorials are scarce
- Compile times
- Unstable API
- UI is hard

The main pain points for me have been that Bevy currently has a very lackluster UI system as of `0.13.1`. I know there are plans to improve this in the future but for now, it's a bit of a pain to work with. I'm also losing a lot of time due to lack of hot reloading but that is partly my fault. They recommend not using the release flag in development. Though, since my game is rather simple it hasn't been a deal breaker. Most of the time I make rather large changes in which case you do not compile that often anyway.

The biggest boons for me have been the speed of the engine and the fact that it's written in Rust. I have been able to write a lot of the game logic in a very safe way. The ESC system is wonderful, combined with algebraic data types, and treating errors as values I have been able to write very robust code.

On a personal note, I've noticed that I'm gravitating towards tools that are code first. Bevy doesn't have an editor, instead, everything is written in code. Of course, some things are better done in an editor but programming is my main skill so I'm happy to see this trend.
Instead of learning how to use an editor I can reuse my programming skills.
A few other tools that are also code-first are [Manim](https://www.manim.community/), [Motion Canvas](https://motioncanvas.io/), and [Glicol](https://glicol.org/).
Here is an example of a YouTube short I made about [9-slicing images](https://www.youtube.com/shorts/fVKpYgH_Nz0) made with Motion Canvas.

I'm excited to see where this trend will take us! In the meantime, I hope you will check out my game [GLOW](https://store.steampowered.com/app/2896110/GLOW/) on Steam.

/Cheers
