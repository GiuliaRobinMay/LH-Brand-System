# Matthew — character generation recipe

The comic Matthew, reproducible. **Read this before generating any Matthew image.**

Recovered 29 Aug 2026 after three failed text-only attempts. The reference stills in
`reference/` are the real asset; this file only regenerates them.

---

## The one rule

**Never generate from text alone.** Always attach a reference still.

The original stills were not generated from a prompt — they were made elsewhere (ChatGPT
with six real reference photos) and brought in as files. Every asset since descends from
a picture. A generation with an empty reference slot invents a new man every time.

| Reference | Use for |
|---|---|
| `reference/matthew-comic-fullbody.webp` | standing and full-body poses |
| `reference/matthew-comic-yellow.webp` | desk, laptop, seated scenes |
| `reference/matthew-comic-hearts.webp` | the pop-art / magenta costume variant |

**Getting a reference into Higgsfield from a cloud session:** the network here blocks most
hosts, but `media_import_url` fetches server-side, so a public raw URL works:

```
https://raw.githubusercontent.com/GiuliaRobinMay/lesko-business-landingpage/main/assets/matthew-comic-fullbody.webp
```

Pass the returned `media_id` as `medias: [{role: "image_references", value: <id>}]`.

---

## The four failure modes

Each is independently fatal. All four were hit on 29 Aug.

**1. Empty reference slot.** Nothing holds still between runs. → Always attach a still.

**2. The avoid-list deletes him.** Banning "spiky hair, bared teeth, wide eyes, sharp
features" removes the character — that *is* Matthew. A prompt built on those bans produced
a generic soft grandfather who wasn't him at all. → Keep the avoid-list to one line: text,
watermarks, logos, extra people, photorealism, 3D. **Nothing about his face or hair.**

**3. Wrong format.** Four views crammed into one 16:9 frame leaves each figure a few
hundred pixels tall and the face collapses. → **One pose per image, square 1:1.** Build a
set by re-running with a different scene line, never by cramming views into one canvas.

**4. Naming him.** Matthew is a real public figure; naming him makes image models refuse
or quietly degrade. → **Never write his real name** — not in the prompt, not in the
filename, not in the message carrying the prompt. Describe by attributes only.

---

## The rule that fixes the "monster" problem

> Wild hair and a big open laugh are not the problem. **Unsmiling eyes are.**

A wide-open mouth plus flat, staring eyes reads as unsettling. The same open mouth with
**crinkled eye corners, lifted cheeks and raised brows** reads as charming. Keep every
energetic trait — the spikes, the laugh, the long face — and specify the eyes.

---

## Master character block — never edit

Only the scene line changes. If a result drifts off-model, the scene line is at fault.

> A cheerful cartoon character: an energetic elderly man in his early eighties with a long
> expressive face, a high domed forehead and a receding hairline of bright white hair that
> sweeps upward into wild pointed spikes. Warm light skin with deep friendly laugh lines,
> prominent cheekbones, a strong chin and large ears. His eyes are large, bright blue and
> crinkled at the outer corners with genuine delight, thin white eyebrows arched high, seen
> through oversized eyeglasses with thick tangerine-orange rims and turquoise-blue temple
> arms. He wears a wide open joyful laugh that lifts his cheeks — playful and mischievous,
> like a man about to share a wonderful secret. He wears a bright yellow single-breasted
> suit jacket and matching yellow trousers printed all over with bold black question marks
> in varying sizes and rotations, a black shirt underneath printed with large flat
> multicoloured polka dots in red, blue, green, yellow and magenta, and a yellow belt with
> a gold buckle. Drawn as clean 2D vector comic-book art: bold black outlines of even
> weight, flat cel-shaded colour with minimal soft shading and small white highlights,
> bright saturated palette, no gradients, no photographic texture, even flat lighting,
> crisp linework.

## New still — edit the scene line only

```
Keep this exact character and art style from the reference image.
[MASTER CHARACTER BLOCK]
SCENE: <one sentence of what he is doing>.
Square 1:1 composition, single character only, full figure cut out on a pure white
background, no props beyond those named. Three small amber-orange triangular spark marks
near his raised hand. High resolution, crisp vector linework, 4K.
Avoid: text, watermarks, logos, extra people, photorealism, 3D render.
```

Model: `nano_banana_pro`, `aspect_ratio: "1:1"`, `resolution: "2k"`, reference in
`medias` with role `image_references`.

## Animation — the formula that worked

```
Comic book cartoon animation, clean flat 2D style matching the reference image exactly.
<one or two sentences of motion, present tense>. Plain warm cream-white background, no
text anywhere, smooth cartoon motion, character stays perfectly on-model. The clip loops
seamlessly with the start and end pose identical.
```

Seedance 2.0, 8 seconds, 1080p, the approved still as start image. Drop the loop sentence
for one-way shots. Three phrases do the real work — **matching the reference image
exactly**, **stays perfectly on-model**, **no text anywhere**. Keep all three, always.

Animate from an approved still, never from text.

---

## The character, read off the live assets

| | |
|---|---|
| **Face** | Long oval face, high domed forehead, receding hairline. Prominent cheekbones, strong chin, large ears with long lobes. Deep laugh lines bracketing the mouth, crow's feet at the eyes — aged but lively. |
| **Eyes** | Large, bright blue, wide with delight and crinkled at the outer corners. Thin white brows arched high. Fully visible through the lenses. |
| **Expression** | A wide open laugh showing upper teeth, cheeks lifted. Mischievous and delighted. Never serene, never blank-eyed. |
| **Hair** | Bright white, swept upward and outward into distinct pointed spikes, each strand outlined. |
| **Glasses** | Oversized, thick tangerine-orange rims, turquoise-blue temple arms. Rectangular or round — both appear across the set. |
| **Rendering** | Clean 2D vector comic art. Bold black outlines of even weight, flat cel-shaded fills, minimal soft shading, small white highlights. No gradients, no texture, no 3D. |
| **Effects** | Exactly three small amber-orange triangular spark marks near the raised hand or head. The set's signature. |
| **Format** | Square 1:1, single figure, cut out on pure white, occasional soft grey contact shadow, no text anywhere. |

## Costumes

**A — Yellow (signature).** Yellow suit covered in bold black question marks. Black shirt
with large flat polka dots in red, blue, green, yellow, magenta. Yellow belt, gold buckle.

**B — Pop-art.** Magenta patchwork jacket with hearts and colour blocks, purple polka-dot
sleeves, black shirt with oversized hearts, pink rectangular glasses.

Planned additions, each mapped to a job: blue (teach), green (celebrate), dark (protect).

---

## Operating order

1. Open with a reference image.
2. Paste the master block, then write one scene line.
3. One square pose per image. No turnaround sheets, no 16:9 for character art.
4. Avoid-list stays one line. Nothing about his face or hair.
5. Never write his real name anywhere in the prompt path.
6. Animate from the approved still, never from text.
7. **Save every keeper into `reference/`.** The library of approved stills is the real
   asset; the prompt only regenerates it.
