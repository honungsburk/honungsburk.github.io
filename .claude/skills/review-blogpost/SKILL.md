---
name: review-blogpost
description: >
  Review and critique a blog post draft. Use when the user wants feedback on a blog post,
  wants to improve a draft, or asks to review/proofread/edit an article. Triggers on phrases
  like "review this post", "give me feedback", "proofread", "review blogpost", "check my draft",
  or "/review-blogpost". Can be pointed at any .md file in content/posts/.
---

# Review Blogpost

Provide a structured, honest review of a blog post draft.

## Workflow

### 1. Identify the post

If the user doesn't specify a file, list `tmp-*.md` files in `content/posts/` and ask which one to review. If there's only one `tmp-` file, use that.

### 2. Read the full post

Read the entire file. Note the frontmatter fields (title, description, tags, date).

### 3. Produce the review

Write a review covering each section below. Be direct and specific — quote the problematic text, explain why it's an issue, and suggest a concrete fix. Skip sections where there are no issues.

#### Title & Description

- Does the title accurately reflect the content?
- Is it compelling enough to click on?
- Is the description a good one-sentence summary?
- Suggest alternatives if improvements are possible.

#### Argument & Structure

- Is the core argument clear? Can you state it in one sentence?
- Does the post flow logically from one point to the next?
- Are there logical gaps, unsupported claims, or contradictions?
- Are there sections that could be cut without losing anything?
- Does the opening hook the reader? Does the ending land?

#### Clarity & Conciseness

- Flag sentences that are confusing, ambiguous, or too long.
- Identify paragraphs that repeat the same point.
- Spot jargon or terms that need explanation for the target audience.
- The blog favors short, punchy paragraphs — flag any that run too long.

#### Grammar, Spelling & Word Choice

- Correct grammar and spelling errors.
- Flag awkward phrasing or word choices.
- Note inconsistent tone or register shifts.
- Check punctuation (especially comma splices, which are common in drafts).

#### Voice & Tone

The blog's voice is: conversational, direct, opinionated, concise. Posts often use personal anecdotes and concrete examples. Flag anything that feels generic, overly formal, or like filler.

### 4. Summary

End with a short summary:

- **Strengths**: 1-2 things the post does well.
- **Priority fixes**: The 2-3 most impactful changes to make first.
- **Overall readiness**: How close is this to publishable? (Early draft / Needs work / Almost there / Ready)
