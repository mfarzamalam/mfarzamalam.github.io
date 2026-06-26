# Farzam Alam — Portfolio

A fast, dependency-free portfolio site (plain HTML + CSS + JS) built to be hosted on
**GitHub Pages** for free. Dark-first design with a light-mode toggle, scroll
animations, and CSS phone mockups for app screenshots.

---

## 1. Add your images

All images live in `assets/images/`. The site works **without** them (it shows tidy
placeholders), but it looks best once you drop yours in. Use these exact filenames:

| File | Where it shows | Suggested size |
|------|----------------|----------------|
| `courtao-1.png` | Hero phone (right side) | App screenshot, **1080 × 2340** (9:19.5) |
| `courtao-2.png` | CourtAo project — front phone | same |
| `courtao-3.png` | CourtAo project — back phone | same |
| `attendx-1.png` | AttendX project — front phone | same |
| `attendx-2.png` | AttendX project — back phone | same |
| `profile.jpg`   | About section photo | square, ~800 × 800 |
| `og.png`        | Social-share preview (optional) | 1200 × 630 |

> Tip: phone screenshots should be **full-bleed app screens** (no device frame baked in)
> — the site draws the phone frame around them. PNG with the exact name = it appears
> automatically. PNG vs JPG: rename the `<img src=...>` in `index.html` if you change the
> extension.

### Add a demo video (optional but recommended)

The hero phone will **autoplay a short looping video** if you provide one. Drop a file at:

```
assets/videos/courtao-demo.mp4
```

Until that file exists, the hero shows the `courtao-1.png` screenshot (the poster) — so nothing
looks broken. As soon as the `.mp4` is committed, it plays automatically.

**Recording tips:** keep it **under 10 seconds**, **no audio** (it plays muted), MP4 / H.264,
portrait, and ideally under ~5 MB so it loads fast. A screen recording of the app (iOS:
built-in screen record; Android: `adb` or the phone's recorder; or the running APK in an
emulator) works great.

---

## 2. Personalize the text

Open `index.html` and tweak as needed. Things you may want to change:

- **Links** — search for `github.com/mfarzamalam`, `mailto:mfarzamalam@gmail.com`, and the
  LinkedIn `https://www.linkedin.com/` placeholders and point them at your real profiles.
- **Experience dates/titles** — see the `EDIT the dates/titles` comment in the Experience
  section.
- **App store links** — if CourtAo / AttendX go live on the stores, add badge links inside
  each `.project__links` block.

Brand colors / fonts live at the top of `css/styles.css` (the `:root` block) — change
`--accent` and `--accent-2` to re-theme the whole site.

---

## 3. Deploy to GitHub Pages (free)

This folder is named `mfarzamalam.github.io` so it deploys to your **root** GitHub Pages
URL: `https://mfarzamalam.github.io`.

```bash
cd mfarzamalam.github.io
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/mfarzamalam/mfarzamalam.github.io.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch
→ Branch: `main` / `(root)` → Save.** Your site is live at
`https://mfarzamalam.github.io` within a minute or two.

> Using a **different** repo name (e.g. `portfolio`)? The site still works — it'll live at
> `https://mfarzamalam.github.io/portfolio/`. All paths in this project are relative, so
> no changes are needed.

### Custom domain (optional)
Add a `CNAME` file containing your domain (e.g. `farzam.dev`) and configure DNS per
GitHub's docs.

---

## Project structure

```
mfarzamalam.github.io/
├── index.html          # all the content
├── css/styles.css      # design system + layout
├── js/main.js          # theme toggle, scroll reveal, mobile nav, tilt
├── assets/
│   └── images/         # ← your screenshots + photo go here
├── .nojekyll           # serve files as-is, skip Jekyll
└── README.md
```

No build step, no dependencies. Edit a file, commit, push — it's live.
