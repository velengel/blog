---
name: blog-review
description: Review draft blog posts in this repository from an engineer-reader perspective. Use when the user asks for a blog review, 技術ブログレビュー, エンジニア視点のレビュー, 良い点と改善点, article polish, or wants prioritized feedback on posts under content/posts before publishing.
---

# Blog Review

## Overview

Use this skill to review blog drafts as publishable technical/personal engineering posts. Prioritize concrete reader value, article structure, and this repository's existing tone over generic prose polishing.

## Review Workflow

1. Read the target Markdown post and nearby relevant examples under `content/posts/`.
2. Check generated context only when useful: title, date, tags, images, `<!--more-->`, Hugo shortcodes, and whether `hugo` output needs updating.
3. Lead with findings, ordered by reader impact. Use file/line references.
4. Separate high-value content feedback from mechanical textlint/style issues.
5. Keep suggested edits specific enough that the author can apply them directly, but do not rewrite the whole article unless asked.

## Review Lens

Evaluate the post through these lenses:

- **Reader promise:** The first few paragraphs should make clear why the article exists and what the reader will get.
- **Engineer value:** Identify where the post teaches a reusable engineering idea, workflow, model, tradeoff, debugging move, or implementation lesson.
- **Specificity:** Flag claims that are interesting but under-specified. Ask for one concrete example, command, artifact, diagram, or before/after when it would materially improve the article.
- **Continuity with existing posts:** Preserve the blog's direct, personal, lightly informal style. Prefer concise bullets and concrete episodes over generic polished prose.
- **Tone alignment:** Keep strong personal reactions when they carry the article, but soften wording that creates unnecessary opposition or distracts from the technical point.
- **Structure:** Check whether sections progress naturally from context -> motivation -> observations -> specific examples -> takeaways/TODO.
- **Summary break:** For published posts, check whether `<!--more-->` is placed so list pages show a useful teaser without swallowing the entire article.
- **Assets and embeds:** Check image paths, alt text, X/Hugo shortcode behavior, and whether generated `docs/` output must be rebuilt.

## Common High-Value Feedback

Use these patterns when they match the draft:

- If a paragraph says "this is a good learning topic", ask what makes it a good learning topic: bounded scope, visible feedback, existing correct answers, debuggability, or connection to daily work.
- If the author mentions using Codex/AI, ask for the actual prompt shape, review loop, artifact, or workflow boundary so readers can reuse it.
- If the post says a session/demo was good, ask what changed in the author's mental model or next action.
- If the article references a conference or event, connect the personal experience to technical takeaways without erasing the personal voice.
- If TODOs are listed, check whether they are concrete enough to be credible next actions.

## Output Shape

Use this shape unless the user asks otherwise:

```text
改善点
- [file:line] Finding. Why it matters. Suggested direction.

良い点
- What is already working and should be preserved.

優先して直すなら
1. Highest leverage edit.
2. Next edit.
3. Optional polish.
```

If there are no serious issues, say that clearly and mention any remaining verification gaps such as `hugo`, image rendering, X embeds, or textlint.
