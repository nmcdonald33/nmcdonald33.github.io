# Natalie McDonald — Portfolio

A clean, static HTML/CSS/JS portfolio site, deployable to GitHub Pages for free.

## Files

```
natalie-portfolio/
├── index.html     ← all content lives here
├── style.css      ← all styles
├── script.js      ← mobile menu + scroll animations
├── resume.pdf     ← ADD THIS: drop your resume PDF here
└── README.md
```

## Deployment (GitHub Pages)

1. Create a new GitHub repository named `yourusername.github.io`
   - Example: `nmcdonald33.github.io`

2. Clone it locally:
   ```bash
   git clone https://github.com/yourusername/yourusername.github.io
   ```

3. Copy all files from this folder into the cloned repo

4. Add your resume PDF as `resume.pdf` in the root folder

5. Push to GitHub:
   ```bash
   git add .
   git commit -m "Initial portfolio"
   git push
   ```

6. Go to your repo → Settings → Pages → Source: Deploy from branch `main`

7. Your site is live at `https://yourusername.github.io` within ~2 minutes.

## Customization guide

### Add your photo
In `index.html`, add this inside `.hero-text` after `.hero-label`:
```html
<img src="photo.jpg" alt="Natalie McDonald" style="width:80px; height:80px; border-radius:50%; object-fit:cover; margin-bottom:1rem;" />
```

### Add project images
Replace each `.proj-card` opening with:
```html
<article class="proj-card">
  <img src="images/project-name.jpg" alt="..." style="width:100%; height:160px; object-fit:cover; border-radius:8px; margin-bottom:1rem;" />
  ...
```
Put images in an `/images/` folder.

### Add a GitHub link
In the `.hero-pills` section, find the placeholder and add your URL:
```html
<a href="https://github.com/yourusername" class="pill" target="_blank">GitHub</a>
```

### Update "Download résumé" button
The button already links to `resume.pdf` — just drop your PDF in the root folder.

### Add project links / case study pages
For each project card, add a link before the closing `</article>`:
```html
<a href="projects/3dpac.html" class="btn btn-ghost" style="align-self:flex-start; margin-top:auto;">Read more →</a>
```

### Colors
Edit these CSS variables at the top of `style.css`:
- `--accent`: main green color (`#2a5f4f`)
- `--ink`: text color (`#1a1814`)
- `--paper`: background (`#faf9f7`)

### Print / PDF version
The site already has print styles. To generate a clean PDF:
- Open in Chrome → File → Print → Save as PDF
- Or use: `Cmd+P` → More settings → No headers/footers
