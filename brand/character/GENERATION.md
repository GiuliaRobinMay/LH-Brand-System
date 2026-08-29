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

## The five-slot prompt — the working template

The original kit had one master block plus a scene line. That locks identity but leaves
no room for a wardrobe. The working structure splits it into five slots: two you never
touch, two you swap, one fixed render spec.

```
Use the reference image ONLY for the character's face, hairstyle, glasses design and
drawing style. Do NOT copy the reference pose, the reference costume, or the reference
body proportions — all three are different here, as described below.

CHARACTER (identical to the reference): [never edit — see the master block above]

PROPORTIONS — THE MOST IMPORTANT INSTRUCTION: he is a VERY TALL, lean, lanky man, drawn
at eight heads tall. His legs are long and take up clearly more than half of his total
height, measured from the ground to his high waistline. His head is SMALL relative to his
body. Long slim arms, narrow shoulders, slender build, long straight legs. He must read
unmistakably as a tall lanky elderly gentleman. He is absolutely NOT short, NOT stocky,
NOT chibi, NOT big-headed; his legs are never short or stubby and his torso is never squat.

COSTUME (new — not the reference costume): [from COSTUMES.md]

POSE (new — not the reference pose): [one sentence]

Drawn as clean 2D vector comic-book art: bold black outlines of even weight, flat
cel-shaded colour with minimal soft shading and small white highlights, bright saturated
palette, no gradients, no photographic texture, even flat lighting, crisp linework.
[FRAMING — see below]. Single character only, cut out on a pure white background. Three
small amber-orange triangular spark marks near his raised hand. High resolution, crisp
vector linework, 4K.

Avoid: text, watermarks, logos, extra people, photorealism, 3D render.
```

| Slot | Changes? |
|---|---|
| Opening instruction | never |
| CHARACTER | never — identity |
| PROPORTIONS | never — build |
| COSTUME | per costume, from `COSTUMES.md` |
| POSE | per image |
| Render + framing | never |

Model: `nano_banana_pro`, `resolution: "2k"`, reference in `medias` with role
`image_references`.

## Framing — the fifth failure mode

**Full-body poses use a 2:3 portrait frame. Square is only for chest-up crops.**

Three separate rounds produced a short, stubby Matthew before the real cause showed up:
a wide arm-span in a square frame forces the model to scale the whole figure down to fit,
and short legs are the result. No amount of "tall" in the prompt beats the frame. The
original stills never had this problem because they are chest-up crops.

- Full body → `aspect_ratio: "2:3"`, plus:
  *"Tall portrait composition; the standing figure fills the entire height of the tall
  frame from the top of his hair to the soles of his shoes, with only a small even margin
  above and below."*
- Chest-up → `aspect_ratio: "1:1"`
- Keep arms fairly close to the body on standing poses so the silhouette stays narrow.

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

**See `COSTUMES.md` for the three approved costumes, the wardrobe rules, and what was
tried and rejected.**

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
