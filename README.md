# 🎡 Hero Roulette — MLBB Draw Tool

A single-file, mobile-friendly web app that randomly draws a **Mobile Legends: Bang Bang** hero, filterable by **lane** or **role**. Built with plain HTML/CSS/JS — no build step, no dependencies.

**🔗 Live site:** [https://mlbbroullete.my.id](https://mlbbroullete.my.id)

![status](https://img.shields.io/badge/status-active-2bcf9e) ![type](https://img.shields.io/badge/stack-HTML%2FCSS%2FJS-cda45e)

---

## ✨ Features

- **Filter by lane** — Exp Lane, Mid Lane, Jungle, Gold Lane, Roam (multi-select)
- **Filter by role** — Tank, Fighter, Assassin, Mage, Marksman, Support (multi-select)
- **Animated draw** — the portrait flickers rapidly through the filtered pool, slowing down before landing on the pick
- **Draw history** — last 10 picks shown as a scrollable strip
- **134 heroes**, roster current as of August 2026, including recent & upcoming additions (Hirara, Marcel, Kalea, Sora, Obsidia, Zetian, Collie — flagged with a `NEW` badge)
- **Placeholder-first images** — every hero falls back to a generated initials badge until you drop in real artwork
- Fully responsive, works on mobile out of the box
- Zero dependencies beyond two Google Fonts

---

## 🚀 Getting started

This is a static site — no build tools required.

```bash
git clone https://github.com/<your-username>/hero-roulette.git
cd hero-roulette
```

Then just open `mlbb-hero-roulette.html` in a browser, or serve it locally:

```bash
python3 -m http.server 8080
# visit http://localhost:8080/mlbb-hero-roulette.html
```

---

## 🖼️ Adding hero artwork

All portraits are placeholders by default (a colored initials badge per hero). To use real art:

1. Create an `images/` folder next to `mlbb-hero-roulette.html`.
2. Add one image per hero, named exactly after its **slug**, e.g.:

   ```
   images/hayabusa.jpg
   images/yi-sun-shin.jpg
   images/chang-e.jpg
   images/popol-and-kupa.jpg
   ```

3. Refresh the page — images are picked up automatically, no code changes needed.

> The full list of slugs used lives in the `HEROES` array near the bottom of the HTML file.

Portrait art is not bundled with this repo. Please source it yourself and make sure you have the rights to use it (see [Disclaimer](#-disclaimer) below).

---

## 🌐 Deployment

Since it's a single static HTML file, it can be hosted anywhere that serves static files:

- **GitHub Pages** — push to a repo, enable Pages on the branch/folder, done.
- **Netlify / Vercel / Cloudflare Pages** — drag-and-drop deploy or connect the repo.
- **Any shared hosting / VPS** — upload `mlbb-hero-roulette.html` (renamed to `index.html` if desired) plus your `images/` folder.

This project is currently deployed at **[https://mlbbroullete.my.idmlbbroullete.my.id](https://mlbbroullete.my.id)**.

---

## 🛠️ Customizing

- **Hero list / roles / lanes** — edit the `HEROES` array in the `<script>` block.
- **Colors / theme** — CSS custom properties are defined at the top of the `<style>` block (`--gold`, `--emerald`, role colors, etc.).
- **Draw speed / flicker count** — tweak `totalTicks` and `delay` inside the `spin()` function.

---

## ⚠️ Disclaimer

This is an unofficial, fan-made tool and is **not affiliated with, endorsed by, or sponsored by Moonton**. *Mobile Legends: Bang Bang* and all associated hero names, characters, and artwork are trademarks/copyrights of Moonton. This project only provides an open-source draw/roulette mechanic — no official game assets are included in the repository.

---

## 📄 License

Code in this repository is provided under the MIT License (add a `LICENSE` file if you want this formalized). Hero artwork is **not** covered by this license and remains the property of its respective owner.
