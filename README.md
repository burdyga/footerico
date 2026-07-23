# Footerico

Hand-tuned brand logos for website footers, emails, and signatures.

Pick a matching style once, paste a live PNG URL, and keep the marks current when brands rebrand—without redeploying local files. No API key.

**Live:** [footeri.co](https://footeri.co)  
**Icon Picker:** [footeri.co/icon-picker.html](https://footeri.co/icon-picker.html)  
**API docs:** [api.footeri.co/](https://api.footeri.co/)

---

## What it does

Footerico turns curated SVG brand marks into styled PNGs:

- ~90 brands (social networks, messengers, files, and more)
- 28 styles (flat, circle / rounded / square, border variants, brand colors and mono)
- Optical centering and hand-made masks for monochrome

**Who it’s for:** marketers, web and email developers, designers who need one consistent social row across site, mail, and signature.

---

## Quick start

1. Open the [Icon Picker](https://footeri.co/icon-picker.html)
2. Choose brands and a style
3. Copy live PNG URLs or embed snippets
4. Paste into your website footer, email, or signature

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
| **[Issues](../../issues)** | Bugs, missing brands, incorrect marks, API problems |
| **[Discussions](../../discussions)** | Ideas, how-to questions, show & tell |


---

## Brand & trademarks

Brand logos belong to their respective owners. Footerico provides styled PNG delivery for practical use in footers and similar placements; it does not claim ownership of third-party marks.

---

## Links

| | |
|--|--|
| Product | https://footeri.co |
| About | https://footeri.co/about.html |
| API docs | https://api.footeri.co |
| API base | https://api.footeri.co |
