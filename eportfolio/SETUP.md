# Git Setup & Deployment Guide

Follow these steps exactly to set up Git and deploy your site to GitHub Pages.

---

## Step 1 — Install Prerequisites

```bash
# 1. Install Quarto
# Download from: https://quarto.org/docs/get-started/

# 2. Install Python packages
pip install numpy pandas plotly scikit-learn

# 3. Add FontAwesome extension (run inside project folder)
quarto add quarto-ext/fontawesome
```

---

## Step 2 — Initialise Git

```bash
cd eportfolio

git init
git add .
git commit -m "Initial commit: Quarto ePortfolio scaffold"
```

---

## Step 3 — Create GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Name it `eportfolio` (or any name you like)
3. Set it to **Public**
4. **Do NOT** initialise with a README (you already have one)

```bash
git remote add origin https://github.com/yourusername/eportfolio.git
git branch -M main
git push -u origin main
```

---

## Step 4 — Add Your Personal Details

Before rendering, update these placeholder values:

| File | What to change |
|---|---|
| `_quarto.yml` | Your name, GitHub URL, LinkedIn URL |
| `index.qmd` | Your name, university, skills |
| `about.qmd` | Your actual background and skills |
| `contact.qmd` | Your email, LinkedIn, GitHub links |
| `reflection.qmd` | Your personal reflection text |
| `cv/` | Add your actual CV as `cv/cv.pdf` |
| `images/` | Add `profile.jpg`, `favicon.png`, `logo.png` |

---

## Step 5 — Add Images

You need three images in the `images/` folder:

- `profile.jpg` — Your professional headshot (square crop recommended)
- `favicon.png` — 32×32 px icon (generate at [favicon.io](https://favicon.io))
- `logo.png` — Site logo for navbar (create at [Adobe Express](https://express.adobe.com) or [Canva](https://canva.com))

Project cover images (optional but recommended):
- `project-sales.png`
- `project-clustering.png`

---

## Step 6 — Render the Site

```bash
quarto render
```

This outputs everything to the `docs/` folder.

```bash
git add .
git commit -m "Render site to docs/ folder"
git push
```

---

## Step 7 — Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages**
3. Under *Source*, select:
   - Branch: `main`
   - Folder: `/docs`
4. Click **Save**

Your site will be live at:
`https://yourusername.github.io/eportfolio`

(Takes 1–2 minutes to deploy the first time.)

---

## Step 8 — Ongoing Workflow

```bash
# Make changes to .qmd files
quarto render          # re-render
git add .
git commit -m "Describe what you changed and why"
git push               # site updates automatically
```

---

## Good Commit Message Examples

```
Add K-Means clustering project with Plotly 3D scatter
Fix navbar CV link to open in new tab
Update about page with internship experience
Add Google Font import to styles.scss
Apply flatly Bootswatch theme with custom SCSS variables
Improve reflection page with task checklist and chart
```

---

## Common Issues

| Problem | Fix |
|---|---|
| Site shows 404 | Wait 2 min; check Pages settings (branch=main, folder=/docs) |
| Plotly charts blank | Ensure `plotly` is installed: `pip install plotly` |
| SCSS not applying | Check for syntax errors; use `quarto preview` to see errors |
| Images not showing | Check file paths — they're case-sensitive |
| FontAwesome icons missing | Run `quarto add quarto-ext/fontawesome` in project root |
