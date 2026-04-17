# The Ezra Centre

> *Transforming man from the core.*

The official website of The Ezra Centre — a teaching and formation ministry equipping the saints for spiritual maturity and fruitfulness.

**Anchor verse:** *"For Ezra had prepared and set his heart to seek the Law of the Lord, and to do and teach in Israel its statutes and its ordinances."* — Ezra 7:10

---

## 🏗  Structure

```
ezracentre/
├── index.html          # Homepage
├── about.html          # About / Story / Founders / Values
├── programs.html       # Programs & Events
├── donate.html         # Partner / Donate
├── books.html          # Books & Resources
├── blog.html           # Journal / Writing
├── contact.html        # Contact / FAQ
├── styles.css          # Shared design system
├── 404.html            # Not-found page
├── images/             # Logo + founder photos
└── README.md
```

No build step. No frameworks. Pure HTML, CSS, and a little JavaScript. Opens in any browser.

---

## 🚀  Deploy to GitHub Pages

### 1. Create a new GitHub repository

Go to [github.com/new](https://github.com/new) and create a repo. You can name it anything — `theezracentre` is a good choice.

### 2. Push this folder to GitHub

From inside this folder, open a terminal and run:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

Replace `YOUR-USERNAME` and `YOUR-REPO` with your actual GitHub username and the repository name you chose.

### 3. Turn on GitHub Pages

1. In your repo on GitHub, click **Settings** → **Pages** (in the left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Choose **Branch: main** and **Folder: / (root)**
4. Click **Save**

Within a minute or two, your site will be live at:

```
https://YOUR-USERNAME.github.io/YOUR-REPO/
```

### 4. (Optional) Add a custom domain

If you own `theezracentre.org` or any domain:

1. In your domain registrar, add a CNAME record pointing to `YOUR-USERNAME.github.io`
2. Edit the `CNAME` file in this folder and put your domain on a single line (e.g. `theezracentre.org`)
3. Commit and push the change
4. In GitHub → Settings → Pages, enter your domain under **Custom domain** and tick **Enforce HTTPS**

GitHub will provision a free SSL certificate automatically (this can take up to 24 hours).

---

## ✏️  Making edits

Everything is editable in any text editor. The most common edits:

| What to change | Where |
|---|---|
| Colors, fonts, spacing | `styles.css` — all tokens are defined in `:root` at the top |
| Homepage hero text | `index.html` — look for the `<!-- HERO -->` section |
| Events list | `programs.html` — look for `<!-- EVENTS LIST -->` |
| Book titles & prices | `books.html` — look for `<!-- LIBRARY -->` |
| Blog articles | `blog.html` — look for `<!-- ARCHIVE -->` |
| Contact info, office hours, FAQ | `contact.html` |
| Partnership tiers & amounts | `donate.html` |
| Footer content (all pages) | search for `<!-- FOOTER -->` in each file |
| Logo | replace `images/logo-color.png` |

After editing, commit and push:
```bash
git add .
git commit -m "Updated homepage copy"
git push
```
Your changes go live within a minute.

---

## 🔌  What still needs backend integration

These are front-end UI only — the forms don't submit anywhere yet. When you're ready, plug them in:

### Donation form (`donate.html`)
Wire up **Paystack** or **Flutterwave** for Nigerian card payments. Both offer plug-and-play JS snippets.

### Newsletter (`index.html`)
Point the form at **Mailchimp**, **ConvertKit**, **Beehiiv**, or **Resend Audiences**. All give you a hosted form endpoint.

### Contact form (`contact.html`)
Easiest options without a backend:
- **Formspree** — free tier, just change `<form action="...">` to their endpoint
- **Web3Forms** — similar, free
- **Netlify Forms** — if you later switch hosts

### Blog
The blog cards currently link to `#`. When you have real articles, either:
- Write each post as an individual HTML file and link to it, or
- Move the blog to a lightweight CMS like **Notion + Super**, **Ghost**, or **11ty** and redirect the blog page

---

## 🎨  Design system

- **Display font:** Cormorant Garamond
- **Editorial / italic:** Fraunces
- **Body:** DM Sans
- **Dominant color:** Deep purple `#3D0F5C`
- **Canvas:** Cream `#F5EFE4`
- **Accent:** Gold leaf `#D4A537`
- **Ink:** `#1A0F20`

All tokens live as CSS variables at the top of `styles.css`. Change them there once and the whole site updates.

---

## 📄  License

© The Ezra Centre. All rights reserved.
