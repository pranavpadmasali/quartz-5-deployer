---
title: Welcome & how this works
description: The 2-minute tour of writing and publishing with Quartz.
date: 2026-07-16
tags:
  - meta
  - getting-started
---

This is a real blog post. It lives at `content/posts/welcome.md`. Here's everything you need to know to run your blog.

## Writing a post

Create a new `.md` file anywhere under `content/`. Most people keep posts in `content/posts/`. Start each file with **front matter** — the block between the `---` lines at the top:

```yaml
---
title: My first post
description: A short summary (used for previews and social cards).
date: 2026-07-16
tags:
  - life
  - ideas
---
```

Then write your post in [Markdown](https://www.markdownguide.org/basic-syntax/) below it. That's it.

## Publishing

There's **no build step to remember**. When you commit and push (or edit a file directly on GitHub), a GitHub Action rebuilds the site and publishes it. Refresh your site a minute later and your changes are there.

Want to hide a draft? Add `draft: true` to its front matter and it won't be published:

```yaml
---
title: Not ready yet
draft: true
---
```

## Linking between notes

Use Obsidian-style wikilinks to connect posts — for example `[[posts/markdown-and-features]]` renders as [[posts/markdown-and-features|this link]]. Backlinks and the graph view are generated for you automatically.

## What to change next

- `quartz.config.yaml` → `pageTitle`, footer links, and (optionally) theme colours.
- `content/index.md` → your home page.
- Delete these sample posts once you've got the hang of it.

Next, take a look at the [[posts/markdown-and-features|features showcase]] to see what your content can do.
