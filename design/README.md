# Design canvases

Source artboards for the published design canvases. **These are the working files** —
every change re-seeds a fresh canvas from them; never edit a seeded output file.

## Lesko Help Brand Sheet — the whole system

https://claude.ai/code/artifact/a3981870-642c-4d0b-ac19-b58f12bba2b3

| Artboard | What it is |
|---|---|
| `Main.dc.html` | Cover |
| `Story.dc.html` | 01 · The story — villains, character, guide, voice |
| `Colour.dc.html` | 02 · Colour — both tiers, use/never pairings |
| `Type.dc.html` | 03 · Typography — Anton + DM Sans, H1 to meta |
| `Character.dc.html` | 04 · The character — costumes, form rules, wardrobe rules |
| `Components.dc.html` | 05 · Components — buttons, seven-step spine, callouts, cards, space icons |
| `Banners.dc.html` | 06 · Community surfaces — banners at true proportion, logo, header, badge |
| `Guide.dc.html` | Applied · Quick Guide page, A4 794 × 1123 |
| `Article.dc.html` | Applied · Article header, 16:9 (exports at 2560 × 1440) |
| `Quote.dc.html` | Applied · Member quote, square post |

`img/` holds downsampled JPEGs of the character reference stills, embedded into the
canvas. Originals live in `brand/character/reference/`.

## Lesko Help Type System — typography only

https://claude.ai/code/artifact/4b106fd0-4a12-4f4d-b3a3-1629fb8c18aa

Uses `Type.dc.html`, `Guide.dc.html`, `Article.dc.html`, `Quote.dc.html`.

## Re-seeding

Edit the `.dc.html` files, then from this folder:

```bash
SKILL="<design skill dir>"
node "$SKILL/seed-canvas.mjs" --template "$SKILL/payload.template.html" \
  --out lesko-brand-sheet.html --title "Lesko Help Brand Sheet" \
  --artboard Main.dc.html --artboard Story.dc.html --artboard Colour.dc.html \
  --artboard Type.dc.html --artboard Character.dc.html --artboard Components.dc.html \
  --artboard Banners.dc.html --artboard Guide.dc.html --artboard Article.dc.html \
  --artboard Quote.dc.html \
  --image img/matthew-comic-fullbody.jpg --image img/matthew-comic-yellow.jpg \
  --image img/matthew-comic-hearts.jpg \
  --canvas canvas.json
```

Then republish the same file path to keep the same URL.

Seeded `.html` outputs are ~2.5 MB of editor payload each and are **not committed** —
they are generated, not authored. See `.gitignore`.

## Open for sign-off

Two devices were introduced here and are not yet approved:

- **The `LESKO?HELP` wordmark** — Anton, question mark in yellow. Taken from the existing
  Quick Guide masthead but never confirmed as the lockup.
- **The question mark as a universal system icon** — space icons, badges, callout markers,
  banner pattern. Follows from the character rules but is its first use as a system
  device rather than a costume print.

## Lesko Direction — Objects (exploration)

https://claude.ai/code/artifact/0b42bd47-69ad-491f-a5ee-7721d329cd10

The chosen visual direction, from Giulia's picks in the inspiration round: **Slush**
("Your money. Unstuck.") and **Tines** — huge display type, floating cut-out objects,
lots of air.

| Artboard | What it is |
|---|---|
| `Main.dc.html` | Hero, light ground |
| `Alt.dc.html` | Hero, saturated blue ground |
| `Objects.dc.html` | The object library — eight objects, drawn as inline SVG |
| `Banner.dc.html` | Applied · Space banner tall, 1560 × 334 |
| `Post.dc.html` | Applied · Social post 1080 × 1080, the anti-scam line |

Layout manifest: `canvas-direction.json`.

### The object library

Every object names something real in the member journey — that is what stops it being
generic startup confetti:

question mark (asking) · heart (from the card suits) · telephone (the call) ·
envelope (the answer that arrives) · house (housing, rent) · call sheet (step 2) ·
his glasses · key (the hidden door)

**How objects behave:** flat fill, one brand colour each, bold black outline of even
weight. Scattered with generous air, rotated a few degrees so they feel dropped rather
than placed. **Never more than six on a surface, never overlapping the type.** They fill
the air around the message; they never compete with it.

### Open decisions

- Light ground or saturated ground
- Whether these are the right eight objects
