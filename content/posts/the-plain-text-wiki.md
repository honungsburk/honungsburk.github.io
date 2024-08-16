+++
title = "The Plain Text Wiki"
date = 2024-08-16

[extra]
modified = 2024-08-16
tags = ["plain-text", "documentation"]
authorURL = "https://frankhampusweslien.com/"
author = "Frank Hampus Weslien"
twitterAuthorID = "@HampusFrank"
description = "Why companies should use plain text wikis."
+++

Every company I've worked for has had an internal wiki for essential information, like how to take sick leave, understand the harassment policy, and access other common procedures. Tools like Confluence and SharePoint are popular for this purpose. But what if we took a different approach and used plain text, hosting everything in a Git repository?

Imagine a single repository dedicated to your internal wiki that you can pull down and explore using [Obsidian](https://obsidian.md/), a powerful note-taking and knowledge management app that stores everything in plain markdown. Not only could you view the content, but you could also easily edit it with Obsidian’s WYSIWYG editor. Avoiding reliance on corporate tools offers significant advantages. When everything is in plain text, you can easily feed it into an LLM to get answers to questions about sick leave or pension plans. Or, if you need to extract some information, you can simply write a Python script. Plus, you can still use your favorite command-line tools like `sed`, `grep`, and `find`. If you want users to have read-only access, you could host the wiki on a subdomain, making it widely accessible while maintaining a detailed history of all changes.

While this approach might not be ideal for most companies, I’d consider it, especially in the early stages when it’s acceptable for only the technical team to manage updates. As the company grows and more people join, for whom learning Git might be too much to ask, we could write a script to push the wiki into a more user-friendly tool.

The larger takeaway is that storing data in a simple format makes it easy to adapt to new situations. If you hand your data over to another company’s tool, you risk getting locked in, making it harder for you and your team to adapt to changing needs.

---

Note: The inspiration for this blog post came from the excellent YouTube channel _No Boilerplate_ and his video on [The Unreasonable Effectiveness of Plain Text](https://www.youtube.com/watch?v=WgV6M1LyfNY).
