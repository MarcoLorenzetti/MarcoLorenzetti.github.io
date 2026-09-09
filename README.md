# Marco Lorenzetti — Personal Portfolio

Personal portfolio website for Marco Lorenzetti, a Physics of Data student at
the University of Padova. The site presents his background and five featured
projects spanning computer vision, deep learning, unsupervised learning,
sports analytics and software engineering.

## Stack

- HTML5 (semantic, accessible markup)
- CSS3 (custom properties, CSS Grid/Flexbox, `clamp()` for fluid type, no framework)
- Vanilla JavaScript (no build step, no dependencies)

No React, Vue, Next.js, or bundler is used — the site is fully static and
self-contained. All project illustrations are hand-built inline SVG, so
there are no external image dependencies.

## Folder structure

```text
MarcoLorenzetti.github.io/
│
├── index.html          → all page markup and content
├── style.css            → full design system (variables, layout, components)
├── script.js             → nav behaviour, scroll reveal, mobile menu
├── README.md
│
└── assets/
    ├── icons/
    │   └── favicon.svg   → site favicon (M monogram)
    ├── profile/           → reserved for a profile photo / OG image, if added
    ├── projects/          → reserved for future project screenshots
    └── illustrations/     → reserved for future custom artwork
```

## Run locally

No build step is required. Just open `index.html` directly in a browser, or
serve the folder with any static file server, e.g.:

```bash
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Deployment (GitHub Pages)

1. Unzip this folder.
2. Initialise (or reuse) the repository `MarcoLorenzetti.github.io`.
3. Push the contents of this folder to the `main` branch:

   ```bash
   git init
   git remote add origin https://github.com/MarcoLorenzetti/MarcoLorenzetti.github.io.git
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git push -u origin main
   ```

4. In the repository settings, under **Pages**, make sure the source is set
   to deploy from the `main` branch, root folder. For a `username.github.io`
   repository this is usually enabled automatically.
5. Visit `https://marcolorenzetti.github.io/`.

## Notes / things to customise

- The **LinkedIn** link is left as a placeholder (`href="#"`) in both the
  hero, contact section and footer — search for `LinkedIn` in `index.html`
  and replace it with the real profile URL.
- The **CV** link in the hero is commented out — add a `cv.pdf` file under
  `assets/` and uncomment the corresponding line in `index.html` if/when a
  CV becomes available.
- An Open Graph image is referenced at
  `assets/profile/og-image.png` but not included — add one (recommended
  1200×630) for richer link previews on social platforms, or remove the
  `og:image` meta tag in `index.html`.
