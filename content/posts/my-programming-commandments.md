+++
title = "My Programming Commandments"
date = 2025-03-09

[extra]
modified = 2025-03-09
tags = ["programming"]
authorURL = "https://frankhampusweslien.com/"
author = "Frank Hampus Weslien"
twitterAuthorID = "@HampusFrank"
description = "Guiding principles that lead me to write better code"
+++

These are my programming commandments. 
They’re not a treasure map that guarantees success, but they’re a solid compass that keeps me heading in the right direction. 
Over time, I’ve found that sticking to these makes my code easier to maintain, reason about, and extend. So here they are:

### 1. Prefer local state to global state
Global state is that one friend who always crashes on your couch and messes up your stuff. Keep it local whenever possible. Your future self (and your teammates) will thank you.

### 2. Prefer immutable to mutable
Mutability leads to spooky action at a distance. 
If something shouldn’t change, don’t let it. Immutable data is predictable, safe, and easier to debug.

### 3. Prefer composition over inheritance
Inheritance can be a trap. Before you create another subclass, ask yourself: could this be done with composition instead? Most of the time, the answer is yes.

### 4. Prefer purity to impurity
Pure functions are little islands of sanity in an ocean of side effects. They take input, return output, and don’t mess with the world in between.

### 5. Parse, don’t just validate
Validating says, “This input is wrong.” Parsing says, “Let’s turn this into something useful.” The latter is way more helpful.

### 6. Try to make as much as possible run locally
Relying on remote services slows you down. If you can develop, test, or prototype locally, do it.

### 7. Automate the repetitive stuff
If you’ve done it twice, script it. If you’ve done it three times, make it a proper tool. Your time is too valuable for manual drudgery.

### 8. Test early, test often
Tests are like seatbelts: annoying until you need them. Write them before you regret not having them.

### 9. Write code for humans
Code is read way more often than it’s written. Make it clear, make it simple, and make it make sense.

### 10. YAGNI (You Ain’t Gonna Need It)
That feature you’re “pretty sure” you’ll need later? You probably won’t. Solve today’s problems today.

### 11. Premature optimization is the root of all evil
Fast code is good, but maintainable code is better. Optimize when it actually matters.

### 12. Are they similar or are they the same?
Not all duplication is bad. Only share code when changing one part means you must change the other.

### 13. The Rule of ThreeIf 
you see a pattern once, ignore it. Twice? Keep an eye on it. Three times? Now it’s time to refactor.

### 14. Refactor as you go
Bad code gets written. The trick is to not leave it bad. Refactoring a little at a time prevents big rewrites later.

### 15. Never fail silently
Silent failures are the worst. If something breaks, scream about it—log it, throw an error, do something! Debugging ghosts is not fun.