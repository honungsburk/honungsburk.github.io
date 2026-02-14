+++
title = "Going Full Agentic"
date = 2026-02-14

[extra]
modified = 2026-02-14
tags = ["programming", "ai"]
authorURL = "https://frankhampusweslien.com/"
author = "Frank Hampus Weslien"
twitterAuthorID = "@HampusFrank"
description = "How structured context turned mediocre AI output into production-quality code."
+++

When I joined Upptec in October 2024, I got a Cursor license. Previously, I had only used Copilot — useful, but not revolutionary.

Over 2025, I gradually learned where AI shines and where it falls apart. I leaned heavily on tab completion, then started using the chat interface more and more, though I was still hand-picking which files to reference. A real shift came when the agents gained a planning mode. That extra reasoning step improved quality enough that I could throw harder problems at them, as long as they weren't too complex.

But the past week changed everything. My team started fully leaning into agentic workflows, and the true unlock turned out to be skills and MCP servers — giving the AI structured context so it produces the right diff. I was blown away by the quality improvement, even using the same model.

I'm going full agentic.

#### Why Elixir works for agents

We write Elixir at Upptec, and it turns out Elixir is surprisingly well suited for agentic workflows. This might sound like cope from an Elixir dev, but hear me out.

Functional code has a property that matters a lot for AI agents: local reasoning. When a function takes inputs and returns outputs without mutating state elsewhere, an agent can reason about that function in isolation. It doesn't need to hold the entire application in its head. Cause and effect are right there, next to each other.

Functional code is also easier to test. This matters because agents love loops — write code, run tests, fix failures, repeat. The tighter that feedback loop, the better the output. Pure functions with clear inputs and outputs make for dead simple test cases.

Dashbit (the company of José Valim, creator of Elixir) wrote a [great post about why Elixir works well with AI](https://dashbit.co/blog/why-elixir-best-language-for-ai). Worth a read.

Then there's [Tidewave](https://tidewave.dev/), an MCP server for Elixir that's genuinely brilliant. It lets your AI agent tap into runtime information from the running application — query the database, read logs, execute code, find documentation. Having that kind of introspection available to an agent is a game changer.

#### Where it fell apart

But Elixir being agent-friendly doesn't mean all Elixir code is agent-friendly.

We have some older projects where the agents produced genuinely nasty code. The worst offender: LiveView components. The agents kept misunderstanding that LiveView components don't have their own process. They'd send messages everywhere, creating spaghetti that no human would ever write. In clean codebases, the agents sang. In messy ones they made the mess worse.

The fix came from my colleague who added a bunch of skills and MCP servers to our setup — giving the agents better context about how our codebase actually works. The quality improvement was immediate and obvious. Agents are only as good as the context you give them.

#### Optimizing the workflow

So the agents work. Now the question is: how do I get more out of them?

We have a custom MCP server at work built with the [Anubis framework](https://github.com/zoedsoupe/anubis-mcp), but it's buggy. The framework itself needs work. That's near the top of my list — a reliable MCP server makes everything else better.

Then there are all my other development tools. Right now I use VS Code. It's comfortable — nice diff view, file tree on the left, Claude in a vertical split, terminal at the bottom. Everything visible at once. But if I want to run multiple agents simultaneously, a GUI editor starts feeling like a bottleneck. I might need to take another look at workflows that stay 100% within the terminal. Using a combination of Neovim and tmux, it might be possible to create a much more integrated experience.

Another question is how multiple agents work on the same project at the same time. Some people use git worktrees. Others just clone the repo into multiple folders. I haven't settled on an answer yet.

But that's what 2026 is about: going from managing one agent to managing many. I'm ready to build.

/Cheers
