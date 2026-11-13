# Footerico

One styled row of icons for website and email footers, plus signatures.

Pick your brands, set a style, copy live PNG URLs. When a brand redraws its logo, the file behind the URL is updated, so your icons never show last year’s mark. No API key.

**Live:** [footeri.co](https://footeri.co/)  
**Icon Picker:** [footeri.co/icon-picker](https://footeri.co/icon-picker)  
**API docs:** [api.footeri.co](https://api.footeri.co/)  
**Release notes:** [footeri.co/release-notes](https://footeri.co/release-notes)

---

## What it does

Footerico turns hand-curated SVG brand marks into styled PNGs:

- 75+ hand-tuned icons (social networks, messengers, files, and more)
- 100 ready styles: flat, filled and outlined shapes (circle / rounded / square)
- Separate colors for the logo and the shape, logo scale inside the shape
- Optical centering and hand-made masks for monochrome

**Who it’s for**

| Role | Why |
|------|-----|
| Marketers | Website footers, email footers, and signatures stay in sync after every rebrand |
| Web developers | Live `<img>` URLs instead of a folder of PNGs in the repo |
| Email developers | PNGs that still render where SVG fails |
| Designers | One look for the whole row, optically balanced |

---

## Quick start

1. **Style your icons** — open the [Icon Picker](https://footeri.co/icon-picker), pick brands, then shape, colors, and size
2. **Copy the live URLs** — plain API links, or ready-made embed snippets
3. **Paste them into your footer or signature** — the same URL keeps serving the current logo

Example:

```html
<img
  src="https://api.footeri.co/icons/instagram.png?size=64&shape=circle&bgcolor=brand&color=white"
  alt="Instagram"
  width="64"
  height="64"
/>
```

---

## Ask your AI agent

The Footerico skill lets Claude and other agents that support Agent Skills build icon links for you. Ask in plain words, for example *“Instagram and LinkedIn icons in a black circle, 32px”*, and get a preview, a link and ready `<img>` code for each icon.

Install with one command:

```bash
npx skills add https://footeri.co/skills/footerico-icons.zip
```

Or [download the skill (.zip)](https://footeri.co/skills/footerico-icons.zip) and upload it in the Claude app (Settings → Skills). Update later with `npx skills update`. Details: [api.footeri.co/#ai-skill](https://api.footeri.co/#ai-skill)

---

## HTTP API

**Base URL:** `https://api.footeri.co`  
**Auth:** none  
**CORS:** `Access-Control-Allow-Origin: *`

| Endpoint | Returns |
|----------|---------|
| `GET /categories` | Category list (JSON) |
| `GET /brands` · `?category=messengers` | Brand catalog (JSON) |
| `GET /icons/{brandId}.png` | Styled PNG |

### Icon query parameters

| Param | Default | Notes |
|-------|---------|--------|
| `size` | `64` | `16`–`128` (UI steps: 16 / 32 / 64 / 128) |
| `shape` | *(flat)* | `circle`, `round`, `square` |
| `color` | `brand` | Logo color: `brand`, `black`, `gray`, `white`, hex `RRGGBB` (no `#`), or `transparent` (logo cut out of a filled shape) |
| `bgcolor` | `gray` (`brand` with `border`) | Shape color: `brand`, `black`, `gray`, `white`, or hex `RRGGBB`. Fill, or the outline with `border`. Shapes only |
| `scale` | `100` | Logo size inside the shape, `75`–`120` (%). Shapes only |
| `radius` | ~10 @ 64px | For `shape=round` only |
| `border` | off | Flag: `border` or `border=true`. Draws the shape as an outline |
| `retina` | off | 2× PNG; keep `width`/`height` at logical `size` |

### Examples

```
https://api.footeri.co/categories
https://api.footeri.co/brands?category=messengers
https://api.footeri.co/icons/telegram.png
https://api.footeri.co/icons/telegram.png?size=32&shape=circle&bgcolor=brand&color=white&retina
https://api.footeri.co/icons/instagram.png?size=64&shape=round&border&bgcolor=black&color=black
https://api.footeri.co/icons/youtube.png?size=64&shape=square&bgcolor=111111&color=transparent&scale=110
```

Interactive docs: [api.footeri.co](https://api.footeri.co/)

---

## Terms of use

Footerico is free for personal and non-commercial use, and paid for commercial use (a business’s website, emails and employee signatures, or agency and freelance work for paying clients). Paid plans aren’t available yet, so commercial use is free for now; there will be at least 30 days’ notice before a plan is required. Full text: [footeri.co/terms](https://footeri.co/terms)

---

## Community

| Channel | Use for |
|---------|---------|
| **[Icon request](../../issues/new?template=icon-request.md)** | Missing brands |
| **[Report a bug](../../issues/new?template=bug_report.md)** | Incorrect marks, API problems |
| **[Feature request](../../discussions/new?category=ideas)** | Ideas and feedback |
| **[Discussions](../../discussions)** | How-to questions, show & tell |

Please search existing Issues and Discussions before opening a new one.

### Before you report a bug

Include:

- Brand id (e.g. `telegram`) and the full icon URL
- Expected vs actual result (screenshot helps)
- Where you use it (website footer / email footer / signature) and client if relevant

---

## Brand & trademarks

Brand logos belong to their respective owners. Footerico provides styled PNG delivery for practical use in footers and signatures; it does not claim ownership of third-party marks.

---

## Links

| | |
|--|--|
| Product | https://footeri.co/ |
| Icon Picker | https://footeri.co/icon-picker |
| Guides | https://footeri.co/guides |
| Release notes | https://footeri.co/release-notes |
| About | https://footeri.co/about |
| Terms of Use | https://footeri.co/terms |
| API docs | https://api.footeri.co/ |
| API base | https://api.footeri.co |
