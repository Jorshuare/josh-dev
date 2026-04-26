---
title: "Assignment 2: Static Blog Setup & Deployment Report"
date: 2026-04-26
draft: false
slug: "assignment-2-report"
description: "A full walkthrough of how I built and deployed this static blog for Assignment 2."
tags: ["assignment", "hugo", "git", "deployment"]
---

## Overview

This report documents the full process of setting up, building, and deploying this static personal
blog website as part of Assignment 2. The site is built with Hugo and the PaperMod theme,
version-controlled with Git, and deployed via GitHub Pages.

---

## Step 1: Create GitHub Account & Repository

The first step was creating a GitHub account to host the project remotely. I then created a new
public repository to serve as the home for the blog's source code. GitHub was chosen because it
integrates directly with GitHub Pages, making deployment straightforward.

---

## Step 2: Install Hugo

Hugo was installed locally using Homebrew:

```bash
brew install hugo
```

Hugo was chosen as the static site generator because:
- It is fast and lightweight
- Content is written in plain Markdown
- The course website itself is built with Hugo, making it a relevant learning tool
- It has a large theme ecosystem

---

## Step 3: Initialize the Project — Commit 1

After installing Hugo, I created a new site and initialized a Git repository:

```bash
hugo new site josh-blog
cd josh-blog
git init
git add .
git commit -m "Initial Hugo site setup"
```

**Rationale:** This first commit captures the clean project scaffold before any customization —
a logical and clean starting point for the version history.

---

## Step 4: Add PaperMod Theme — Commit 2

The PaperMod theme was added by cloning it into the `themes/` directory:

```bash
git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1
```

The `hugo.toml` configuration file was then updated to activate the theme and set basic site
parameters including the site title, author name, and display settings.

```bash
git add .
git commit -m "Add PaperMod theme and configure site"
```

**Rationale:** Separating the theme setup into its own commit keeps the history clean and makes
it easy to identify exactly when and how the theme was introduced.

---

## Step 5: Add README — Commit 3

A `README.md` file was added to the root of the project to describe the repository — what it is,
how to run it locally, and what technologies it uses. The repository was also cloned to confirm
the remote connection was working correctly.

```bash
git add README.md
git commit -m "Add README describing the project"
git push origin main
```

**Rationale:** A README is standard practice for any repository. It makes the project
understandable to anyone visiting the GitHub page, including the course instructor.

---

## Step 6: Add Content & Assignment 1 Report — Commit 4

With the site structure in place, I focused on content. This included:

- Writing the homepage introduction post
- Adding the Assignment 1 Markdown report as a blog post so it is accessible from the site
- Previewing everything locally using Hugo's development server:

```bash
hugo server -D
```

The `-D` flag renders draft posts, which is useful for previewing content before publishing.

```bash
git add content/
git commit -m "Add assignment report and homepage content"
git push origin main
```

**Rationale:** Content is the core purpose of the blog. Grouping the initial content additions
into one commit reflects a complete, logical unit of work.

---

## Step 7: Add About Page, Blog Posts & Navigation — Commit 5

To improve the site's completeness and meet the assignment rubric, I added:

- An **About page** introducing myself and the blog's purpose
- Two additional blog posts documenting my learning journey
- Navigation menu links configured in `hugo.toml` pointing to About, Posts, and Assignment 1

```bash
git add .
git commit -m "Add About page, blog posts, and navigation menu"
git push origin main
```

**Rationale:** This commit brings the site to a fully functional state — navigable, personal,
and meeting all content requirements for the assignment.

---

## Tools & Frameworks Used

| Tool | Purpose |
|------|---------|
| Hugo | Static site generator |
| PaperMod | Hugo theme for clean blog layout |
| Git | Version control |
| GitHub | Remote repository hosting |
| GitHub Pages | Free static site deployment |
| Markdown | Content authoring format |

---

## Reflection

Building this blog reinforced several things I've been learning in my Software Engineering
program. Using Git with intentional, meaningful commits — rather than just saving changes —
made the development process feel more structured and professional.

Hugo's Markdown-based workflow is a good fit for technical documentation and blogging. The
barrier to publishing is low, which means the focus stays on the content itself.

The most challenging part was configuring the GitHub Actions deployment pipeline, but once it
was working, the feedback loop of push → auto-deploy became satisfying to use.
