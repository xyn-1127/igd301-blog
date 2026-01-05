---
title: "Lab 1 — Setup Course Blog"
date: 2025-12-15
draft: false
tags: ["IGD301", "lab", "setup", "blog"]
---

## Overview

In this first lab, I set up a public course blog that will host all lecture and lab homeworks for IGD301.  
My goals were:

- Create a clean, readable blog structure for future posts
- Make local preview easy for fast iteration
- Deploy the site online using GitHub Pages so it is always accessible

---

## Tooling Choice

I used **Hugo** (static site generator) + **GitHub Pages** for hosting.

Reasons:

- Hugo is lightweight and fast to build locally
- Markdown writing is convenient for documenting labs
- GitHub Pages + GitHub Actions provides automatic deployment on every push

---

## Setup Steps

### 1) Create the Hugo project

I created a new Hugo site and initialized a git repository:

- `hugo new site igd301-blog`
- `git init`

Then I added a theme (PaperMod) as a git submodule:

- `git submodule add https://github.com/adityatelange/hugo-PaperMod themes/PaperMod`

### 2) Configure the site

I created/updated `hugo.toml` with a minimal configuration:

- Site title
- Theme name
- Menu entry for posts
- `baseURL` pointing to my GitHub Pages address

### 3) Write the first post

I created the first blog post:

- `hugo new posts/lab1-setup-blog.md`

Then I wrote this post to document what I did and any issues.

### 4) Local preview

To preview the blog locally:

- `hugo server -D`

This starts a local server (default: `http://localhost:1313/`) and hot-reloads changes, which is very convenient when writing posts.

---

## Deployment (GitHub Pages)

### 1) Create a GitHub repository

I created a public repository on GitHub:

- Repo name: `igd301-blog` (project page)
- Default branch: `main`

Then I pushed the local project to GitHub.

### 2) Deploy with GitHub Actions

In the repository settings, I enabled **Pages** and selected **GitHub Actions** as the deployment source.

I added a workflow file at:

- `.github/workflows/hugo.yml`

This workflow:

1. Checks out the repository (including submodules for the theme)
2. Installs Hugo (extended version)
3. Builds the site into the `public/` folder
4. Uploads the build artifact and deploys it to GitHub Pages

After the workflow finished successfully, GitHub generated a public Pages URL.

---

## Result

- **Website:** https://xyn-1127.github.io/igd301-blog/  
- **Repository:** https://github.com/xyn-1127/igd301-blog  


---

## Issues & Notes

- **Base URL matters:** If `baseURL` is not set correctly, the theme CSS may not load and links can be wrong.  
  I fixed this by setting:

  `baseURL = "https://xyn-1127.github.io/igd301-blog/"`

- **Theme submodule:** Using a theme as a git submodule keeps the theme version controlled and reproducible, but it also means the workflow needs `submodules: recursive` in the checkout step.
