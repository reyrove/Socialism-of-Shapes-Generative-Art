# Socialism of Shapes — Generative Art

> A seed-based generative system for collective pattern compositions.  
> A reproducible catalogue of computational shape studies.

---

## What is this?

**Socialism of Shapes** places a single mode of shape across a grid — triangles, squares, rectangles, arcs, or mixed — and then gives every cell its own expression. Each shape is drawn at its own angle, its own size, its own colour, its own weight, its own glow. No two are identical, yet all share the same underlying rule.

Every artwork in this catalogue is defined by a single numeric seed. The same seed always produces the identical composition — making each piece **traceable, reproducible, and licensable** across textile, print, and apparel applications.

Named for the tension between uniformity and individuality, **Socialism of Shapes** reframes the collective pattern as a textile.

---

## Live

🌐 **[View the catalogue →](https://reyrove.github.io/Socialism-of-Shapes/)**

---

## The System

The generator combines two layers:

| Layer | Description |
|-------|-------------|
| **Grid** | A seeded lattice of cells whose spacing and size are both derived from the seed. |
| **Shapes** | One of 16 shape modes fills every cell, each cell drawn with its own angle, size, colour, weight, and glow. |

Both layers are driven by the same seed, ensuring deterministic output.

### Parameters

- **Shape modes** — 16 (triangles, squares, rectangles, arcs, mixed, etc.)
- **Grid spacing** — `w / (random × 40 + 10)` pixels
- **Cell size** — `w / (random × 40 + 20)` pixels
- **Line weight** — `w / (random × 600 + 200)` pixels
- **Shadow blur** — `w / (random × 70 + 80)` pixels
- **Shadow colour** — 1 of 23 dark tones, chosen per seed
- **Background** — 1 of 22 pastel tones, chosen per seed
- **Foreground palette** — 1 of 45 curated colour sets (2 to 8 colours each)

---

## Structure

```
Socialism-of-Shapes/
├── index.html                       ← Full catalogue (single-file)
├── images/
│   ├── fav.svg
│   ├── shapes-tote.png
│   ├── shapes-cushion.png
│   └── ...
├── Socialism-of-Shapes.jpg          ← Apparel mockup
└── README.md
```

The entire project is contained in a single `index.html` — no build step, no dependencies, no framework. Open it in any modern browser.

---

## Features

- **Seed-based generation** — every composition is deterministic and reproducible
- **Live catalogue** — cover, statement, plate, surfaces, process, archive, commission sections
- **Multiple surfaces** — print, scarf, textile, wallpaper — all rendered from the same seed
- **Archive of 8 seeds** — click any plate to load it into the main view
- **PNG export** — download any composition directly from the browser
- **Keyboard shortcuts** — `R` for new seed, `S` to save
- **Legal modal** — licensing, terms, and credits built in
- **Responsive** — works on desktop, tablet, and mobile
- **Mobile-first navbar** — horizontally scrollable with fade hint
- **Fast load** — master offscreen rendering + cached thumbnails

---

## Usage

### Generate a new composition

Click **New Seed** or press `R`.

### Download the current composition

Click **Download** or press `S`.

### Load a seed from the archive

Click any plate in the **Archive** section.

---

## Color System

Every composition is drawn from three curated palettes, each seeded independently:

**Background — 22 pastel tones**

| Sample names |
|--------------|
| WhiteSmoke · Electric Blue · Magic Mint · Tea Green · Organic Brown |
| Light Orange · Neon Yellow · Sage · Cotton Candy · Donut Pink |
| Rose Quartz · Deep Peach · Coral Peach · Light Beige · Pastel Violet |
| Pastel Pink · Powder Pink · Desert Sand · Cornsilk · Light Slate |
| LightSkyBlue · Robin Egg Blue |

**Shadow — 23 dark tones**

Blacks, night blues, deep teals, muted browns, maroons, purples, wine reds — chosen for the glow behind each shape.

**Foreground — 45 curated palettes**

Each palette contains between 2 and 8 colours chosen for contrast and coherence — neon duos, triad harmonies, quartet contrasts, and larger rainbow sets.

Because all three axes and the per-cell randomness are seeded, no two compositions share the same rhythm of shape and colour.

---

## Technical Notes

- Pure vanilla JavaScript — no libraries
- Canvas 2D rendering
- Custom xorshift random generator for deterministic seeds
- Device-pixel-ratio aware rendering
- Fully static rendering — one seed produces one composition, no animation loops
- **Master offscreen rendering** — the field is drawn once at 1024² and blitted everywhere; cover uses a seed variant with its own cached render
- **Archive thumbnails** — rendered at 320² and cached
- Shape primitives: `Triangle`, `Square`, `Rectangle`, `shapeHelper` (mixed), arc
- `prefers-reduced-motion` respected

---

## About

**Socialism of Shapes** is a project by [Reyhaneh Daneshdoost](https://reyrove.github.io/) — an Iranian-born artist working at the intersection of classical textile logic and generative systems.

The work begins with a simple observation: the woven surface — repetitive, mathematically structured, infinitely variable — has always been a form of computation, long before computers.

**Socialism of Shapes** is an attempt to render that logic visible.

> *Every shape is the same shape — and yet no two are quite alike.*

---

## Licensing

All compositions are seed-documented and available for licensing across textile, surface, and apparel applications.

For commercial use, custom editions, or exclusive rights:

📧 **reyhanehdaneshdoost@gmail.com**

See the **Licensing** section in the live catalogue for details.

---

## Links

- 🌐 [Website](https://reyrove.github.io/)
- 📷 [Instagram](https://www.instagram.com/rey._.rove/)
- 💼 [LinkedIn](https://www.linkedin.com/in/reyhaneh-daneshdoost-730481160/)
- 🐦 [X](https://x.com/reyrove)

---

## Credits

**Design & Generative System**  
Reyhaneh Daneshdoost

**Typefaces**  
Cormorant Garamond · DM Mono

**Edition**  
Socialism of Shapes — Autumn 2026

---

<p align="center">
  <em>Generative Collective Pattern</em><br />
  <sub>© Reyrove Studio · All compositions reproducible by seed</sub>
</p>