# Journalism Portfolio

A clean, minimal portfolio for journalists — built with plain HTML and CSS, hosted free on GitHub Pages.

## File structure

```
journalism-portfolio/
├── index.html              ← Main portfolio page (edit this)
├── css/
│   └── style.css           ← All styles (edit colours/fonts at the top)
├── projects/
│   ├── project-template/   ← Copy this folder for each data project
│   │   └── index.html
│   ├── flood-risk/         ← Example project folder
│   │   └── index.html
│   └── ...
└── README.md
```

---

## How to publish on GitHub Pages (step by step)

### 1. Create a GitHub account
Go to [github.com](https://github.com) and sign up if you haven't already.

### 2. Create a new repository
- Click the **+** button → **New repository**
- Name it exactly: `yourusername.github.io` (replace with your GitHub username)
- Set it to **Public**
- Click **Create repository**

### 3. Upload your files
- On the new repo page, click **Add file → Upload files**
- Drag and drop all the files from this folder
- Click **Commit changes**

### 4. Your site is live!
Wait about 60 seconds, then visit:
`https://yourusername.github.io`

---

## How to edit the portfolio

### Change your name and intro
Open `index.html` and look for the `<!-- HERO -->` section:
```html
<h1>Journalist covering climate, data &amp; policy</h1>
<p>Your one-line bio here.</p>
```

### Add an article clip
Find the `<!-- ADD MORE CLIPS ABOVE THIS LINE -->` comment in `index.html` and paste a new clip block above it:
```html
<article class="clip">
  <div class="clip-body">
    <p class="clip-meta">DD Mon YYYY · Story type</p>
    <a class="clip-title" href="https://full-url-of-article.com" target="_blank" rel="noopener">
      Your article headline here
    </a>
    <p class="clip-pub">Publication Name</p>
  </div>
  <span class="clip-arrow" aria-hidden="true">↗</span>
</article>
```

### Add a data project
1. Copy the `projects/project-template/` folder and rename it (e.g. `projects/my-investigation/`)
2. Edit the `index.html` inside that folder
3. Then add a card in the main `index.html` pointing to it:
```html
<a class="project-card" href="projects/my-investigation/index.html">
  <p class="project-title">My investigation</p>
  <p class="project-desc">What it's about in one or two sentences.</p>
  <span class="project-tag">Tools used</span>
</a>
```

### Change fonts or colours
Open `css/style.css` — the settings block at the top is all you need:
```css
:root {
  --font-body:   Georgia, serif;        /* body text font */
  --color-text:  #111111;               /* main text colour */
  --color-muted: #666666;               /* secondary text */
  --color-bg:    #fafafa;               /* page background */
}
```

### Embed a chart in a project page
The easiest option for beginners is [Datawrapper](https://www.datawrapper.de) (free):
1. Upload your data and create a chart on Datawrapper
2. Click **Publish** → **Embed** → copy the iframe code
3. Paste it inside the `<div class="chart-container">` in your project's `index.html`

Other free options: [Flourish](https://flourish.studio), [Observable](https://observablehq.com), [Infogram](https://infogram.com)

---

## Tips

- Keep your clips in reverse chronological order (newest first)
- Each data project should have a methodology section — it builds credibility
- Link to the GitHub repo for each project's code and data
- Add a `favicon.ico` to the root folder for a browser tab icon
