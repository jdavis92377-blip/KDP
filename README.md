# KDP — Author Book Website

A simple website for my Amazon books. Each book has its own page with its cover,
the back-cover blurb, and a "Buy on Amazon" button. Newest books appear first.

**Live site:** https://jdavis92377-blip.github.io/KDP/

---

## First-time setup (do this once)

1. **Turn on the website:** on GitHub, open this repo → **Settings** → **Pages**.
   Under *Build and deployment* choose **Deploy from a branch**, pick the `main`
   branch and the `/ (root)` folder, then **Save**. After a minute or two the
   site is live at the address above.
2. **Add your details:** open `_config.yml`, click the ✏️ pencil icon, and change
   `title`, `author_name`, `tagline`, `bio`, and (optionally) `amazon_author_url`,
   `contact_email`, and `author_photo`. Click **Commit changes**.
3. **Remove the sample book:** delete `_books/sample-book.md` and
   `assets/covers/sample-cover.svg` once you've added a real book.

---

## Adding a new book (all on the GitHub website, no software needed)

### Step 1 — Upload the cover
1. Go to the `assets/covers` folder.
2. Click **Add file → Upload files** and drag in your cover image (JPG or PNG,
   the same front cover you uploaded to KDP works well).
3. Give it a simple name with no spaces, e.g. `the-silent-shore.jpg`.
4. Click **Commit changes**.

### Step 2 — Add the book details and blurb
1. Go to the `_books` folder.
2. Click **Add file → Create new file**.
3. Name it after the book, ending in `.md`, e.g. `the-silent-shore.md`
   (this also becomes the page address: `/books/the-silent-shore/`).
4. Copy everything from [`BOOK_TEMPLATE.md`](BOOK_TEMPLATE.md), paste it in, and
   fill it in:

```markdown
---
title: "The Silent Shore"
subtitle: "A Novel"
series: "Book 1 of the Harbor Trilogy"
genre: "Mystery"
date: 2026-11-01
cover: /assets/covers/the-silent-shore.jpg
amazon_url: "https://www.amazon.com/dp/B0XXXXXXXX"
---
When the tide goes out, the secrets come in.

Paste the rest of the back-cover blurb here. Leave a blank line
between paragraphs.
```

5. Click **Commit changes**. The site updates itself in about a minute.

### Tips
- The **first paragraph** of the blurb is the hook — it shows on the home page and
  appears larger on the book's own page.
- Leave `amazon_url: ""` empty to show a **Coming soon** badge for a pre-release book.
- Add `published: false` to the top section to hide a book until you're ready.
- `subtitle`, `series`, and `genre` are optional — leave them as `""` if unused.
- To edit a book later, open its file in `_books`, click ✏️, change it, and commit.
- Keep the `---` lines exactly as they are; they separate the details from the blurb.

---

## Previewing on your own computer (optional)

```bash
bundle install
bundle exec jekyll serve
```
Then open http://localhost:4000/KDP/
