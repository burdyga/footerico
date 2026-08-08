# Footerico

One styled row of icons for website and email footers, plus signatures.

Pick your brands, set a style, copy live PNG URLs. When a brand redraws its logo, the file behind the URL is updated, so your icons never show last year’s mark. No API key.

**Live:** [footeri.co](https://footeri.co/)  
**Icon Picker:** [footeri.co/icon-picker](https://footeri.co/icon-picker)  
**API docs:** [api.footeri.co](https://api.footeri.co/)

---

## What it does

Footerico turns hand-curated SVG brand marks into styled PNGs:

- 75+ hand-tuned icons (social networks, messengers, files, and more)
- 28 ready styles (flat, circle / rounded / square, border variants, brand colors and mono)
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

1. **Style your icons** — open the [Icon Picker](https://footeri.co/icon-picker), pick brands, then shape, color, and size
2. **Copy the live URLs** — plain API links, or ready-made embed snippets
3. **Paste them into your footer or signature** — the same URL keeps serving the current logo

Example:

```html
<img
  src="https://api.footeri.co/v1/icons/instagram.png?size=64&shape=circle&color=brand"
  alt="Instagram"
  width="64"
  height="64"
/>
```

---

## HTTP API

**Base URL:** `https://api.footeri.co`  
**Version:** `v1`  
**Auth:** none  
**CORS:** `Access-Control-Allow-Origin: *`

| Endpoint | Returns |
|----------|---------|
| `GET /v1/categories` | Category list (JSON) |
| `GET /v1/brands` · `?category=messengers` | Brand catalog (JSON) |
| `GET /v1/icons/{brandId}.png` | Styled PNG |

### Icon query parameters

| Param | Default | Notes |
|-------|---------|--------|
| `size` | `64` | `16`–`128` (UI free steps: 16 / 32 / 64 / 128) |
| `shape` | *(flat)* | `circle`, `round`, `square` |
| `color` | `brand` | `brand`, `black`, `gray`, `white`, or hex `RRGGBB` (no `#`) |
| `radius` | ~10 @ 64px | For `shape=round` only |
| `border` | off | Flag: `border` or `border=true` |
| `retina` | off | 2× PNG; keep `width`/`height` at logical `size` |

### Examples

```
https://api.footeri.co/v1/categories
https://api.footeri.co/v1/brands?category=messengers
https://api.footeri.co/v1/icons/telegram.png
https://api.footeri.co/v1/icons/telegram.png?size=32&shape=circle&retina
https://api.footeri.co/v1/icons/instagram.png?size=64&shape=round&color=black&border
```

Interactive docs: [api.footeri.co](https://api.footeri.co/)

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
| About | https://footeri.co/about |
| API docs | https://api.footeri.co/ |
| API base | https://api.footeri.co |
