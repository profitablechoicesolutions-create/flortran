# Flortran — Marketing Website

> **Finance. Advice. Transcend.**
>
> A static marketing website for **Flortran Advisory & Consulting**, a luxury financial advisory firm specializing in business valuation, financial modeling, and investment readiness review.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

---

## Table of Contents

- [Overview](#overview)
- [Pages](#pages)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Deployment](#deployment)
  - [GitHub Pages](#deploy-to-github-pages)
  - [Netlify](#deploy-to-netlify)
  - [Vercel](#deploy-to-vercel)
- [Brand System](#brand-system)
- [Customization](#customization)
- [Browser Support](#browser-support)
- [License](#license)
- [Contact](#contact)

---

## Overview

A six-page static site, hand-coded in HTML, CSS, and vanilla JavaScript — no build step, no framework dependencies. Optimized for fast loads, accessibility, and a refined editorial aesthetic befitting a financial advisory brand.

**Design system:** navy & gold luxury palette · Cormorant Garamond display + Inter body type · gold-accented eyebrow labels · circular icon treatment.

---

## Pages

| Page | File | Purpose |
| --- | --- | --- |
| Home | `index.html` | Hero with live valuation card, services overview, case studies preview |
| Services | `services.html` | Service detail, comparison table, "Who this is for" |
| Case Studies | `case-studies.html` | Three detailed client case studies + outcomes |
| Credentials | `credentials.html` | Consulting focus, 6-card credentials grid, FAQ, testimonial |
| Free Resource | `free-resource.html` | Lead-magnet guide download, 5-step flow, LinkedIn CTA |
| Book Consultation | `book-consultation.html` | 30-min consultation request form with details panel |

---

## Tech Stack

- **HTML5** — semantic markup
- **CSS3** — custom properties, CSS Grid, Flexbox, responsive design
- **Vanilla JavaScript** — mobile menu, FAQ accordion, demo form handlers
- **Google Fonts** — Cormorant Garamond, Inter

> No build tooling, no npm install, no transpilation. Edit files and reload.

---

## Project Structure

```
flortran/
├── index.html                  # Home page
├── services.html               # Services page
├── case-studies.html           # Case Studies page
├── credentials.html            # Credentials page
├── free-resource.html          # Free Resource page
├── book-consultation.html      # Book Consultation page
├── css/
│   ├── style.css               # Base styles, header/footer, components
│   └── pages.css               # Page-specific styles
├── js/
│   └── main.js                 # Mobile menu, FAQ, form demo
├── images/
│   ├── logo-light.png          # For light backgrounds (header)
│   └── logo-dark.png           # For navy backgrounds (footer)
├── .gitignore
├── LICENSE
└── README.md
```

---

## Getting Started

### Option 1 — Open directly

Double-click `index.html` to open it in your browser. Internal navigation works via relative paths.

### Option 2 — Local server (recommended)

A local server avoids any CORS quirks and matches production behavior.

```bash
# Python 3
python3 -m http.server 8000

# Node.js (with npx)
npx serve .

# PHP
php -S localhost:8000
```

Then visit **http://localhost:8000** in your browser.

---

## Deployment

### Deploy to GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, choose `Deploy from a branch`.
4. Select branch `main` and folder `/ (root)`. Save.
5. Your site is live at `https://<your-username>.github.io/<repo-name>/`.

**Custom domain:** add a `CNAME` file at the project root containing your domain (e.g. `flortran.com`), and configure DNS at your registrar.

### Deploy to Netlify

1. Push the repo to GitHub.
2. On [netlify.com](https://netlify.com), click **Add new site → Import an existing project**.
3. Connect GitHub and select the repo.
4. Build command: *(leave empty)*. Publish directory: `.`
5. Deploy.

### Deploy to Vercel

1. Install the [Vercel CLI](https://vercel.com/docs/cli): `npm i -g vercel`.
2. From the project folder, run `vercel`.
3. Follow the prompts. No build configuration needed for a static site.

---

## Brand System

### Colors

| Token | Value | Use |
| --- | --- | --- |
| Navy | `#0F2748` | Primary text, dark backgrounds |
| Gold | `#C9A24A` | Accents, CTAs, eyebrow labels |
| Gold Soft | `#f5ecd6` | Tinted card backgrounds |
| Background | `#f7f6f1` | Page background |
| Background Soft | `#faf9f4` | Card backgrounds |
| White | `#ffffff` | Surfaces |
| Border Soft | `#efece2` | Hairlines |

### Typography

- **Display:** Cormorant Garamond (400, 500, 600, 700)
- **Body:** Inter (300, 400, 500, 600, 700)

All design tokens live in `:root` inside `css/style.css` as CSS custom properties — change them once, propagate everywhere.

---

## Customization

### Update brand colors

Open `css/style.css` and edit the variables under `:root {}`:

```css
:root {
  --navy: #0F2748;
  --gold: #C9A24A;
  /* ... */
}
```

### Replace the logo

Drop your own files into `images/` keeping the same filenames:

- `logo-light.png` — appears on light header backgrounds
- `logo-dark.png` — appears on the navy footer background

### Edit copy

Each page is plain HTML. Open the relevant file and edit the text directly.

### Connect forms

The two forms (`free-resource.html` and `book-consultation.html`) carry a `data-demo` attribute and are intercepted by `js/main.js` for a fake "submitted" state. To wire them to a real backend:

- **Formspree** — change the `<form>` tag to `<form action="https://formspree.io/f/YOUR_ID" method="POST">` and remove `data-demo`.
- **Netlify Forms** — add `data-netlify="true"` and `name="form-name"` attributes if hosting on Netlify.
- **Custom API** — replace the demo handler in `js/main.js` with a real `fetch()` call.

---

## Browser Support

Modern evergreen browsers (Chrome, Edge, Firefox, Safari). Uses CSS Grid, Flexbox, and CSS custom properties — supported in all browsers from 2017 onward.

---

## License

This project is released under the [MIT License](LICENSE). The Flortran name, wordmark, and brand identity remain the property of Flortran Advisory & Consulting.

---

## Contact

**Flortran Advisory & Consulting**
*Finance. Advice. Transcend.*

For project inquiries, open an issue or visit the live site.
