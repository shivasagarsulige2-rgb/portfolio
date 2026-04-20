# My ePortfolio

A personal portfolio website built with **Quarto**, managed with **Git**, and published via **GitHub Pages**.

## 🔗 Live Site
[https://yourusername.github.io/eportfolio](https://yourusername.github.io/eportfolio)

## 📁 Structure

```
eportfolio/
├── _quarto.yml          # Site configuration
├── .nojekyll            # Disable Jekyll on GitHub Pages
├── .gitignore
├── index.qmd            # Landing page (About: trestles template)
├── about.qmd            # About me page
├── reflection.qmd       # Module reflection
├── contact.qmd          # Contact & references
├── styles.scss          # Custom SCSS (sass:defaults + sass:rules)
├── images/              # Profile image, favicon, logo
├── cv/                  # CV as PDF + linking page
├── projects/
│   ├── index.qmd        # Projects listing (Quarto listing, grid type)
│   ├── projects.yml     # Project metadata
│   └── list/            # Individual project .qmd files
│       ├── sales-forecasting.qmd
│       └── customer-segmentation.qmd
└── docs/                # Rendered output (do not edit manually)
```

## 🚀 Building Locally

```bash
# Install Quarto: https://quarto.org/docs/get-started/
quarto preview    # live preview
quarto render     # build to docs/
```

## 📦 Dependencies

```bash
pip install numpy pandas plotly scikit-learn
quarto add quarto-ext/fontawesome
```

## 🛠 Tech Stack

- [Quarto](https://quarto.org) — publishing system
- [GitHub Pages](https://pages.github.com) — hosting (docs/ folder, main branch)
- Python (NumPy, Pandas, Plotly, scikit-learn) — data projects
- Bootswatch Flatly theme + custom SCSS
- Google Fonts: DM Serif Display / DM Sans / DM Mono

## 📄 License

© 2025 Your Name. All rights reserved.
