# Ashish Kumar — Portfolio

A fast, dependency-free personal portfolio built with plain **HTML + CSS + vanilla JS**.
No frameworks, no build step — it loads in a single round-trip and scores 100 on Lighthouse
performance when hosted statically.

## Structure

```
Portfolio/
├── index.html        # the whole site (semantic HTML)
├── styles.css        # design system, dark + light themes
├── script.js         # theme toggle, scroll reveal, counters (~4 KB)
├── resume.pdf        # your résumé (linked from the navbar)
└── assets/
    ├── avatar.jpg    # your GitHub profile photo (replaceable)
    └── favicon.svg   # AK monogram icon
```

## Hosting (pick one — all free)

### GitHub Pages (recommended)
1. Create a repository named `ashish-jha-73.github.io` (you already have one!).
2. Push these files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Portfolio site"
   git remote add origin https://github.com/ashish-jha-73/ashish-jha-73.github.io.git
   git push -u origin main
   ```
3. Visit **https://ashish-jha-73.github.io** — done. No settings needed.

### Netlify
Drag & drop this folder onto https://app.netlify.com/drop

### Vercel
`vercel deploy` from this folder, or import the repo at vercel.com.

## Customizing

- **Colors / theme** — edit the CSS variables at the top of `styles.css`.
- **Photo** — replace `assets/avatar.jpg` with any square image.
- **Content** — everything lives in `index.html` with clear section comments.
- **Résumé** — overwrite `resume.pdf`; the navbar link picks it up automatically.

## Performance notes

- Zero JavaScript frameworks; ~4 KB of vanilla JS (`defer`), one CSS file.
- Fonts loaded with `preconnect` + `display=swap`; system fallbacks if offline.
- Hero avatar is local, sized 460px, with `fetchpriority="high"`.
- All icons are inline SVG (no icon font, no extra requests).
- Respects `prefers-reduced-motion`; accessible (skip link, aria labels, focus states).
