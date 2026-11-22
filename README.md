# Quant-aum: how to run this website yourself

This repository **is** the website [quant-aum.com](https://quant-aum.com). Whatever you change here goes live automatically, usually within **1–2 minutes**. You never need special software. A web browser is enough.

---

## The easy way: the visual editor (recommended)

1. Go to **[app.pagescms.org](https://app.pagescms.org)** and click **Sign in with GitHub**.
2. Allow it access to the **quant-aum** repository (only the first time).
3. Open **quant-aum**. You'll see **Blog posts** and **About page** in the menu.

### Write a new post
1. Click **Blog posts → Add an entry**.
2. Fill in:
   - **Title**: the post's headline.
   - **Subtitle**: one line shown under the headline.
   - **Short summary**: 1–2 sentences shown on the blog page and in Google.
   - **Publish date**: today's date.
   - **Small label**: for example `Essay · No. 3`.
   - **Cover image** (optional): upload a picture. If you leave it empty, a default illustration is used.
   - **Post**: write your post like in any word processor, with headings, bold, italics, quotes, links and images.
3. Click **Save**. Within about 2 minutes the post appears on the home page, the blog page and Google's sitemap, with next/previous links. You don't need to touch any other file.

### Edit or delete a post
Open **Blog posts**, click the post, edit, and **Save**. To delete it, use the **⋯** menu next to the post.

### Edit the About page
Open **About page**, edit, and **Save**.

---

## The manual way: editing directly on GitHub

Use this if the visual editor is ever unavailable.

### New post
1. Open the **`_posts`** folder, then click **Add file → Create new file**.
2. Name it in this format: `YYYY-MM-DD-short-title.md`, for example `2026-11-20-shiva-and-shakti.md`.
   The part after the date becomes the web address: `quant-aum.com/blog/shiva-and-shakti.html`.
3. Paste this at the top and fill it in:

```
---
title: "Your post title"
subtitle: "One line shown under the title."
description: "One or two sentences for the blog page and Google."
date: 2026-11-20 10:00:00 +0530
label: "Essay · No. 3"
---

Write your post here. Leave a blank line between paragraphs.

## A section heading

Some **bold** text, some *italic* text, and a [link](https://example.com).

> A quote goes after a > sign.
>
> — *Who said it*
```

4. Click **Commit changes**. Done.

### Writing cheat sheet (Markdown)

| You type | You get |
|---|---|
| `## Heading` | A section heading |
| `### Smaller heading` | A smaller (gold) heading |
| `**bold**` | **bold** |
| `*italic*` | *italic* |
| `[text](https://link)` | a link |
| `> quote` | a large gold-lined quote |
| `- item` | a bullet list |
| `![description](/assets/images/photo.jpg)` | an image (upload it to `assets/images` first) |

Special boxes (copy these exactly):

```html
<div class="note"><strong>Note:</strong> Your text here.</div>

<div class="resonance">
<div><b>Physics</b>The science side.</div>
<div><b>Story</b>The scripture side.</div>
</div>

<div class="divider">· · ·</div>
```

---

## Site settings: name, social links

Open **`_config.yml`** and click the pencil ✏️. You can change the text in quotes:

- `author`: your name, shown on every post and in the footer.
- `youtube`, `instagram`, `spotify`, `x_twitter`, `linkedin`: paste a full profile link (for example `"https://youtube.com/@quantaum"`) and it appears in the footer automatically. Leave it as `""` to hide it.

---

## Which file does what

| File / folder | What it is | Edit it? |
|---|---|---|
| `_posts/` | Your blog posts, one file each | ✅ Yes, freely |
| `about.md` | The About page | ✅ Yes |
| `_config.yml` | Site name, author, social links | ✅ The quoted values |
| `assets/images/` | Pictures you upload | ✅ Yes |
| `index.html` | Home page layout | ⚠️ Carefully |
| `style.css` | Colours, fonts, design | ⚠️ Carefully |
| `_layouts/`, `_includes/` | Page templates (header, footer, post layout, illustrations) | ⚠️ Rarely |
| `.pages.yml` | Settings for the visual editor | ⚠️ Rarely |
| `CNAME` | Connects quant-aum.com | ❌ Never delete |
| `robots.txt` | Tells Google it may index the site | ❌ Leave |

---

## If something goes wrong

- **The change isn't showing.** Wait 2 minutes, then press **Ctrl+F5**.
- **Was it published?** Click the **Actions** tab at the top of this repository. A green ✅ means it went live. A red ❌ means GitHub couldn't build the site, and **your previous version stays live**, so visitors never see a broken site. Click the red item to see which file caused it. It's usually a missing `"` or `---` at the top of a post.
- **Undo a change:** open the file, click **History**, open the previous version, copy it back, and commit. Every change ever made is saved, so nothing is truly lost.
