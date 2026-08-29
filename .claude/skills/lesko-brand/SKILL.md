---
name: lesko-brand
description: The Lesko Help brand pack — World story, vocabulary, colour, type, character rules, voice and anti-patterns. Read this before designing, writing or generating anything for Lesko Help, Matthew Lesko, or the Lesko Help community: flyers, guides, landing pages, social posts, thumbnails, emails, slides, PDFs, community banners, AI imagery. Contains the brand's actual answers; the method for using them is in the `brand-system` skill.
---

# Lesko Help — brand pack

**Status: in progress.** Sections marked 🔒 are settled. Sections marked ⏳ are open
and must not be treated as decided. Never invent a value for an open section — ask.

Read alongside the `brand-system` skill, which holds the method.

---

## 1. The World 🔒

**Villain — two, and both matter.**

*The hidden door.* Money that is legally yours, sitting behind forms, jargon and the
belief that it is not for people like you. Matthew's own origin: *"I got bored of
helping fat cats after a while and thought, why doesn't everyone know this
information?"*

*The parasite.* People who charge for what is free — including impersonators who
pose as Matthew or his team to rob the members he is trying to help. Real losses in
the community: $1,080 to a fake "USAID Grant Administrator", then asked for $4,000
more.

**What's at stake.** The house on Friday. The car that keeps the job. The procedure
Medicare won't cover.

**The main character.** Someone told no so many times they have started saying it to
themselves. The word they use is *desperate*. The word they fear is *stupid*. Often
older, often disabled, often caring for someone else, frequently writing from a phone
and sometimes with no phone at all.

**The guide.** Matthew Lesko. 82. Eccentric on purpose. Members call him *Mr. Question
Man*. The only figure in the category who never asks for more money.

**The practice.** Asking. He does not write your grant — he teaches you to ask, which
is what the question mark has meant all along.

**The promise.** *Don't give up. Somebody will answer.*

**The counter-line to the parasite** — already written by the team, and the strongest
sentence the brand owns:

> Your subscription is all the money he will ever ask for.

---

## 2. Voice 🔒

Native phrases, harvested from members — use these, don't invent replacements:

- *"Don't give up."* / *"Don't give up. Ever."*
- *"Stay safe out there."*
- *"It was right on time."*

Members write in fragments: *"How do I get money."* · *"I'm so confused on how to
navigate."* Write back at that level. Short sentences. One idea per line. No jargon,
no marketing cadence, no cleverness.

**Never:** hype, urgency countdowns, "secrets", implied government affiliation,
guaranteed outcomes, invented dollar figures.

The emotional truth of a win is not the amount — it is that **somebody finally
answered**. Design and copy should feel like a hand raised, not a sales page.

---

## 3. Vocabulary 🔒

Found in the wild, not invented. Use these exact names:

**The Grant Roadmap — seven steps, in order:**

1. Daily Welcome Tour
2. Call Sheet Classes
3. AI Grant Researcher
4. Questions Channel
5. Application Classes
6. Group Coaching
7. Ask Matthew Live

**Other proper nouns:** Navigators (member guides, stipended) · LeskoHelpers
(members) · Quick Guide Library · Success Stories · Safety Warnings · We Care ·
Thursday Drop-In Clinic · Lesko Pro (business hub) · My Grant Buddy (member-facing
AI) · Mr. Question Man (Matthew, member-given).

---

## 4. Character rules 🔒

The brand's character is **illustrated Matthew** — comic-book style, white spiked hair,
oversized orange-and-blue glasses, question-mark suit.

| Form | Where | Why |
|---|---|---|
| **Illustrated Matthew** | The guide inside the product: roadmap steps, guides, thumbnails, teaching, wayfinding | Ownable, reproducible, accessible, impossible to counterfeit |
| **Real Matthew** — genuine photo and video | Proof of a living person: live sessions, testimonials, "this is really him" | Authenticity and warmth |
| **AI-generated photoreal Matthew** | **Never** | It is precisely what the impersonators produce |

That last row is a hard rule, not a preference.

### Generating him 🔒

**Read `brand/character/GENERATION.md` before generating any Matthew image.** It holds the
master character block, the scene-line format, the animation formula, and the four failure
modes that produced a monster and then a stranger on 29 Aug 2026.

The three rules that matter most:

1. **Never generate from text alone.** Always attach a reference still from
   `brand/character/reference/`. The originals were never generated from a prompt.
2. **Never ban his features.** Banning spiky hair, bared teeth, wide eyes or sharp
   features deletes the character. The avoid-list is one line: text, watermarks, logos,
   extra people, photorealism, 3D.
3. **Never write his real name in a prompt.** He is a real public figure; naming him makes
   image models refuse or quietly degrade. Describe by attributes only.

And the rule that fixes the unsettling-face problem: *wild hair and a big open laugh are
not the problem — unsmiling eyes are.* Keep the energy, specify crinkled eye corners,
lifted cheeks and raised brows.

### Costumes 🔒

**Full detail, exact costume lines and wardrobe rules: `brand/character/COSTUMES.md`.**

Three costumes, closed. Each is a signal, not decoration.

| Costume | Shirt | Job |
|---|---|---|
| **Yellow**, black question marks | black + polka dots | Welcome & everyday. The signature. |
| **Blue**, white question marks | black + hearts | Teach & explain — roadmap, classes, guides |
| **Green**, yellow question marks | black + polka dots | Celebrate — Success Stories, wins |

**Wardrobe rules** (each learned from a rejected image): the motif is always question
marks, never blocks or abstract shapes · the shirt ground is always black · the shirt is
never plainer than the suit · nothing corporate below the neck (no ties, no plain black
belt) · one print per costume.

**Not adopted:** orange (blurs the yellow/red safety signals) · the multicoloured
confetti suit (an intricate photographic print that flat comic style cannot reconstruct
from words — needs a photo of the garment as a second reference) · a dedicated Protect
costume (tried in dark navy and red, both rejected; the dark version also dropped his
laugh and read as cold).

⏳ **Protect is an open question, and probably the wrong one.** A warning may be better
served by yellow Matthew beside a red warning graphic than by dressing him for bad news.
Decide deliberately before generating a fourth suit.

### The yellow-suit tension, resolved 🔒

Yellow is both his signature suit and the "pay attention" colour. To keep the signal from
weakening: **the yellow suit is identity, not signal.** The attention role belongs to
yellow *surfaces* — highlighter bars, callout blocks, ink-on-yellow. Suit and surface do
different jobs.

⏳ **Open:** the six-pose set (welcome, point up, present to the side, celebrate, palm out,
at the laptop) as transparent cutouts at one consistent scale.

## 5. Colour 🔒 (values) / ⏳ (application)

**Source of truth: `brand/tokens.css`.** Never hand-write a hex; reference a token.

Eight brand colours, confirmed by Giulia, in three tiers:

| Tier | Colour | Hex | On white |
|---|---|---|---|
| **Primary** | Blue | `#3655b3` | 6.76:1 |
| **Primary** | Yellow | `#fdcc0a` | 1.52:1 |
| Support | Green | `#2ca01c` | 3.41:1 |
| Support | Mid blue | `#0060ff` | 5.10:1 |
| Support | Red | `#f93946` | 3.68:1 |
| Accent | Purple | `#7c3bb0` | 6.75:1 |
| Accent | Pink | `#ff24b1` | 3.42:1 |
| Accent | Teal | `#00d6f6` | 1.76:1 |

**These are a display palette.** Five of the eight cannot legally carry body text
on white, and none reaches the brand's 7:1 floor. That is not a fault — they are
built to be seen, which is right for this brand. The system therefore runs **two
tiers of the same identity**:

- `--display-*` — used exactly as supplied for fills, shapes, illustration,
  Matthew's suits, backgrounds, charts. Never altered.
- `--text-*` — the same hue darkened until it clears 7:1 on white, used only when
  that colour has to carry words.

Nothing about the brand's loudness changes. The text tier exists so words stay
readable for an audience that often cannot read low-contrast type.

**Semantic roles carry over from existing work and must be preserved:** blue =
official and clickable · yellow = pay attention · red = danger and scams · green
= a win.

### Hard pairing rules

| Pairing | Ratio | Rule |
|---|---|---|
| Ink `#0e1a2b` on yellow | 11.50 | **The yellow treatment.** Always ink on yellow. |
| Ink on teal | 9.95 | Fine |
| White on deep red `#b50511` | 7.01 | **Use this for warning banners** |
| White on display blue | 6.76 | Large text only (≥24px) |
| Ink on green | 5.12 | Large text only |
| **Blue on yellow** | **4.45** | **Never.** The two primaries fail against each other — place them side by side, never one on the other. |
| White on display red | 3.68 | Never — the scam warnings are the most safety-critical message in the brand and must not sit at this ratio |

⏳ Still open: proportion and distribution rules (how much of each colour, where),
and per-surface application.

## 6. Typography ⏳

**DM Sans** is the current member-facing choice (Regular / Semi-Bold / Bold /
Ultra-Bold) and is a sound fit: geometric, plain, highly legible, freely licensed.

⚠️ The internal document's typography is **not** a design choice — every font in it
fell back to DejaVu, meaning the intended fonts never embedded. Do not treat it as
reference.

⏳ Type scale, weights and pairing not yet set.

---

## 7. Accessibility floor 🔒

Raised above the default because of who the audience is. These outrank aesthetics.

- Body text **18px** minimum on screen, **12pt** minimum in print
- Contrast **7:1** for body text where achievable, never below 4.5:1
- Hit targets **48px** minimum
- Plain language: short sentences, one idea per line, no jargon
- Never carry meaning by colour alone — always pair with a word or icon
- Assume a phone, an older screen, and a reader who is stressed

---

## 8. Anti-patterns 🔒

Never do these:

- **AI-generated photoreal Matthew.** See section 4.
- **Anything that reads scammy** — urgency timers, "secrets", fake official seals,
  implied government affiliation, guaranteed amounts.
- **Invented dollar figures.** Real and sourced, or bracketed as `[AMOUNT]`.
- **Playing-card suits (♠♥♦♣)** as decoration. They appear in older documents;
  they say luck and gambling. Grants are a learnable process, not a lottery, and
  that framing is the scammer's, not Matthew's. ⏳ Confirm with Giulia before removing
  from any existing template.
- **Small, low-contrast, dense layouts.** They fail this audience specifically.
- **Corporate calm applied to Matthew himself.** The frame gets calm so Matthew can
  stay loud. Never the reverse.

---

## 9. Mandate 🔒

**Modernise the frame, protect the icon.** Matthew, the question mark, the colour and
the warmth stay and get stronger. Everything around them — type, layout, spacing,
hierarchy, accessibility, anti-scam trust signals — is rebuilt to a modern,
high-contrast, plain-language standard. Existing assets get reissued, not discarded.

---

## 10. Open questions ⏳

1. ~~Exact hex values~~ — done, see `brand/tokens.css`
2. Three costume variants + character model sheet
3. Type scale and pairing
4. Card suits — deliberate device or template leftover?
5. Wordmark: `Lesko?Help` (question mark as connector) appears in the Quick Guide —
   confirm whether this is the intended lockup
6. Compliance lines required on public-facing material
