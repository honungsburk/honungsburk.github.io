+++
title = "Cloud in a box"
date = 2025-03-21

[extra]
modified = 2024-07-21
tags = ["programming"]
authorURL = "https://frankhampusweslien.com/"
author = "Frank Hampus Weslien"
twitterAuthorID = "@HampusFrank"
description = "Why we choose microservices, and why we shouldn't"
+++

I've been writing Elixir professionally for a while now, and something's been bugging me: we're not using its coolest feature. The BEAM VM (Erlang's virtual machine) lets you distribute your application across multiple nodes seamlessly, yet most of us still deploy microservices. Why?

Let's look at the common reasons for choosing microservices:

1. "Different services need different languages"
   - Python for ML
   - Rust for performance
   - Node.js because that's what the team knows
   
2. "We need isolation"
   - If one service crashes, others keep running
   - Different teams own different services
   - Separate deployment pipelines

3. "We want clean dependencies"
   - New services start fresh
   - No legacy code
   - Modern libraries

But here's the thing: these are all solvable problems in a monolith.

Need different languages? Write FFI bindings. Yes, it's work, but it's one-time work versus the constant overhead of service boundaries. The BEAM VM already has excellent FFI support for Rust and C.

Worried about isolation? The BEAM VM solved this decades ago. Its actor model and "let it crash" philosophy give you better isolation than network boundaries. Each process is isolated, supervised, and can crash without taking down the system.

Want clean dependencies? That's what modules and proper architecture are for. If you're making microservices to avoid refactoring, you're just pushing the complexity into your network calls.

Team ownership? Use proper modules and interfaces. Conway's Law doesn't mandate network boundaries.

The real reason we choose microservices is that they're easier right now. It's faster to start a new service than to fix the old one. It's easier to use a different language than to write FFI bindings. It's simpler to deploy separately than to figure out proper module boundaries.

But this is death by a thousand cuts. Each service adds:
- Distributed logging
- Service discovery
- Network failure handling
- Deployment pipelines
- Monitoring
- Message serialization
- API versioning

What's the alternative? Languages like Elixir (and experimental ones like Unison) show us a better way: write as a monolith, deploy as distributed. Imagine telling your runtime: "This module needs more CPU" or "This code should run close to the database." No microservices, just deployment annotations.

We need deeper integration between languages and cloud platforms. Our code should be able to dynamically request resources, spawn processes across nodes, and handle distribution - all while looking like local function calls.

The future isn't more microservices. It's better abstractions for distribution, built into our languages and runtimes. We just need to stop taking the easy way out and start building those abstractions.

/Cheers