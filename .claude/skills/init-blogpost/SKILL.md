---
name: init-blogpost
description: >
  Initialize a new blog post for the Zola-based personal blog. Use when the user wants to
  start writing a new blog post, create a draft, or begin a new article. Triggers on phrases
  like "new blog post", "start a post", "write a blog post", "init blogpost", "new article",
  or "/init-blogpost".
---

# Init Blogpost

Create a new blog post draft and help the user shape their initial idea into a clear first draft.

## Workflow

### 1. Create the draft file

1. Ask the user for a **working title** (remind them this is temporary and can change later).
2. Generate a slug from the title (lowercase, hyphens, no special chars).
3. Copy the template into `content/posts/`:

```bash
cp <skill-dir>/assets/template.md content/posts/tmp-<slug>.md
```

The `tmp-` prefix signals work-in-progress. It will be removed when the post is published via a separate skill.

4. Fill in the frontmatter placeholders:
   - `TITLE` → the working title
   - `DATE` → today's date (`YYYY-MM-DD`)
   - `DESCRIPTION` → leave as `"DESCRIPTION"` for now (filled later)
   - `tags` → leave empty for now

### 2. Capture the idea (stream of consciousness)

Ask the user:

> What is this blog post about? Don't worry about structure or phrasing — just dump your thoughts. What's the core idea? Why does it matter? What points do you want to hit?

Let the user write freely. They may send one long message or several. Collect everything before proceeding.

### 3. Rewrite into an initial draft

Take the user's raw thoughts and rewrite them into a clear first draft:

- Preserve the user's voice and opinions — do not sanitize or make generic
- Organize into a logical flow with natural section breaks
- Keep the tone conversational and direct (match existing posts on the blog)
- Aim for concise paragraphs — the blog favors short, punchy writing
- Do NOT add fluff, filler introductions, or generic conclusions
- Write the draft directly into the `tmp-<slug>.md` file after the frontmatter
- Update the `description` field in frontmatter with a one-sentence summary

### 4. Confirm and next steps

After writing the draft, tell the user:

- The draft is at `content/posts/tmp-<slug>.md`
- They can preview it with `zola serve`
- Refinement and publishing are handled by separate skills
