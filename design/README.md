# Design canvases

Source artboards for the published design canvases. **These are the working files** —
every change re-seeds a fresh canvas from them; never edit a seeded output file.

## Lesko Help Type System

https://claude.ai/code/artifact/4b106fd0-4a12-4f4d-b3a3-1629fb8c18aa

| Artboard | What it is |
|---|---|
| `Main.dc.html` | The type scale: H1 → meta, with sizes and rules |
| `Guide.dc.html` | Quick Guide page, A4 794 × 1123 — proves the 12pt print floor |
| `Article.dc.html` | Article header, 16:9 (exports at 2560 × 1440) |
| `Quote.dc.html` | Member quote, square post format |

`canvas.json` lays them out.

## Re-seeding

Edit the `.dc.html` files, then from this folder:

```bash
node "<design skill dir>/seed-canvas.mjs" \
  --template "<design skill dir>/payload.template.html" \
  --out lesko-type-system.html \
  --title "Lesko Help Type System" \
  --artboard Main.dc.html --artboard Guide.dc.html \
  --artboard Article.dc.html --artboard Quote.dc.html \
  --canvas canvas.json
```

Then republish the same file path to keep the same URL.

The seeded `.html` output is ~2.4 MB of editor payload and is **not committed** — it is
generated, not authored. See `.gitignore`.
