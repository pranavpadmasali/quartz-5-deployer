# 🌱 Quartz 5 Blog Boilerplate

Start a beautiful, fast blog in **under 5 minutes** — no coding, no build tools, no design work. Powered by [Quartz 5](https://quartz.jzhao.xyz/) and hosted **free** on GitHub Pages.

Everything good is already switched on: full-text search, graph view, backlinks, dark mode, RSS, LaTeX math, syntax highlighting, social preview images, and more. You just write Markdown.

---

## 🚀 Get your blog online (5 steps)

### 1. Create your repo from this template

Click the green **“Use this template”** button at the top of this page → **Create a new repository**.

Name it:

- **`your-username.github.io`** → your blog lives at `https://your-username.github.io` (recommended), **or**
- **anything else** (e.g. `blog`) → it lives at `https://your-username.github.io/blog`

> Either works. The blog figures out its own address automatically — you never edit a URL.

### 2. Turn on GitHub Pages (one time)

In your new repo, go to **Settings → Pages → Build and deployment → Source** and choose **GitHub Actions**.

> This is the one manual click GitHub requires — it can't be automated for a new repo. Do it once and every future push deploys on its own.

### 3. Make it yours

Open **`quartz.config.yaml`** (edit it right on GitHub — pencil icon ✏️) and change the line:

```yaml
pageTitle: My Quartz Blog     # 👉 your blog's name
```

Commit the change. That's the only edit you *need* to make.

### 4. Wait for the build

Go to the **Actions** tab and watch the “Deploy blog to GitHub Pages” job finish (~1–2 minutes). When it’s green, your blog is live at:

- `https://your-username.github.io` (if you named the repo `your-username.github.io`), or
- `https://your-username.github.io/your-repo-name` (otherwise)

### 5. Write posts

Add Markdown files to the **`content/`** folder (posts usually go in `content/posts/`). Each push republishes automatically. See the included sample posts for the format — then delete them.

That's it. 🎉

---

## ✍️ Writing posts

Create a file like `content/posts/my-first-post.md`:

```markdown
---
title: My first post
description: A one-line summary for previews and social cards.
date: 2026-01-01
tags:
  - life
---

Write your post here in **Markdown**.
```

- **Hide a draft:** add `draft: true` to the front matter.
- **Link between posts:** use `[[posts/my-first-post]]` (wikilinks). Backlinks and the graph build themselves.
- **Images:** drop them anywhere in `content/` and reference them with `![alt](image.png)`.

---

## 🎨 Customising (all optional)

Everything lives in **`quartz.config.yaml`**, which is heavily commented. Common tweaks:

| Want to…                | Change this in `quartz.config.yaml`                     |
| ----------------------- | ------------------------------------------------------- |
| Rename the blog         | `pageTitle`                                             |
| Change brand colours    | `theme.colors` (`secondary` is the accent/link colour)  |
| Change fonts            | `theme.typography`                                      |
| Update footer links     | the `footer` plugin's `links`                           |
| Add analytics           | `analytics:` (Plausible, Google, Umami, GoatCounter…)   |
| Enable comments         | see the **Comments** section below                      |

## 💬 Enabling comments (giscus)

Comments are powered by [giscus](https://giscus.app) (GitHub Discussions). To turn them on:

1. Make sure your repo is **public** and enable **Discussions** (Settings → General → Features).
2. Install the [giscus GitHub App](https://github.com/apps/giscus) on the repo.
3. Visit [giscus.app](https://giscus.app), enter your repo, and copy the generated `repoId` and `categoryId`.
4. In `quartz.config.yaml`, find the `comments` plugin, set `enabled: true`, and fill in the four values.

## 🌐 Custom domain

1. In **Settings → Pages → Custom domain**, add your domain (e.g. `blog.example.com`) and configure DNS as GitHub instructs.
2. In `quartz.config.yaml`, set `baseUrl: blog.example.com` (no `https://`, no trailing slash). The deploy will now use your domain instead of the auto-generated one.

---

## 🖥️ Preview locally (optional)

You don't need this to blog, but if you want to preview before pushing:

```bash
npm install
npx quartz build --serve
```

Then open <http://localhost:8080>. Requires [Node.js 22+](https://nodejs.org).

---

## 🙏 Credits

Built on [Quartz](https://github.com/jackyzha0/quartz) by Jacky Zhao and the Quartz community. This repo just adds sane defaults, one-file configuration, and a zero-config GitHub Pages deploy.

Questions or issues? Open an issue on this repo, or check the [Quartz docs](https://quartz.jzhao.xyz/).
