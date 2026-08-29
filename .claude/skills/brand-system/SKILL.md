---
name: brand-system
description: The method for building and applying a brand system for any client. Use when creating, extending, auditing or applying a brand — logos, palettes, type scales, layouts, imagery direction, guidelines — or when producing any designed asset (flyer, landing page, social post, PDF guide, email, thumbnail, slide) for a brand that has a pack in this repo. Client-agnostic: it defines HOW the work is done. The client's own answers live in a separate `*-brand` pack skill in the same repo.
---

# Brand system method

This is the method, not a brand. It applies to every client. The answers for a
specific brand live in that repo's own pack skill (`<client>-brand`). **Always
read the pack before designing anything.** If no pack exists, build one using
Part 1 before producing assets.

## Two layers, never mixed

| Layer | Lives in | Contains |
|---|---|---|
| **Method** (this file) | every client repo, identical | how to build and apply a brand system |
| **Pack** (`<client>-brand`) | one per client repo | that brand's actual answers |

Never write client facts into this file. Never write method into a pack.

---

## Part 1 — Building a brand system

Work these in order. Skipping straight to visuals produces competent, forgettable work.

### 1. The World (strategy before pixels)

A brand is a world the audience enters, not a look. Establish these before any
design decision, because design is downstream of them:

- **The villain** — what the brand is against. Named, specific, and something the
  founder is genuinely angry about. Abstract villains ("inefficiency") are useless;
  the best ones have a face and a victim.
- **What's at stake** — the concrete loss if nothing changes. Not a feeling; a thing.
- **The main character** — the audience, described as they actually are, including
  what they are afraid of. Use their own words, not a persona document.
- **The guide** — who leads them, and what makes that person credible.
- **The practice** — the repeatable thing the brand teaches. Name it.
- **The promise** — the transformation, in the audience's language.
- **The vocabulary** — the brand's proper nouns: roles, stages, rituals, products.

Two rules that matter more than the framework:

**Harvest, don't invent.** Most live brands already have a vocabulary that grew
organically — in the community, the support inbox, what members call the founder.
Found language beats invented language every time. Search for it before writing any.

**Ground it in evidence.** Where a community, mailing list, support archive or
content library exists, mine it: success stories, complaints, the words people use
when desperate, what the team repeats without being asked. Quote verbatim in the
pack. A World document assembled from evidence is defensible; one assembled from
imagination is a guess.

### 2. Audit what exists

Before proposing anything, extract hard values from real artefacts — source files,
stylesheets, PDFs, live pages:

```bash
pip install --quiet pymupdf   # then extract exact fonts and colours from PDFs
```

Record exact hex values, exact font names and sizes, exact spacing. Never round to
a 4/8px grid, never approximate a colour by eye if the real value is obtainable.

Expect **drift**: the same palette appearing in two or three slightly different
versions across documents. Reconciling drift is usually the single highest-value
act in the whole engagement — the brand often already has the right system, twice.

Also check whether typography in a document was *chosen* or *fell back*. Fonts named
DejaVu, Liberation, Nimbus or Helvetica-substitutes in an extraction usually mean the
intended font failed to embed. That document's type is an accident, not a decision.

### 3. Settle the direction with the client, not for them

Never pick an aesthetic alone. Either ask, or build 2–4 genuinely different low-fi
direction artboards and let them choose something they can see. Each direction gets
an honest name, an honest motivation, and its real tradeoff — a set where only the
favourite has a case made for it is a rigged vote.

Once chosen, stop re-asking. Option names are permanent; never renumber or rename
across turns.

### 4. Define the system

Minimum contents of a finished system:

- **Colour** — one value per role, not a swatch collection. Every colour has a job
  (brand, action, warning, success, attention, surface, text) and a documented
  contrast pair. Semantic colour that the audience already understands (red=danger,
  green=win) is an asset — reconcile it, don't redesign it.
- **Type** — one or two families, a fixed scale, and a minimum size floor set by the
  audience, not by taste. Fallback stacks with close metrics, since exports and
  emails often lose the webfont.
- **Layout** — a grid, a spacing scale, and rules for density.
- **Components** — the recurring objects (button, card, step, warning, callout,
  quote) drawn once, with their states.
- **Imagery** — what kind of image is allowed, what is forbidden, and why. Include
  generation prompts if AI imagery is used, and a character model sheet if the brand
  has a character.
- **Voice** — how it talks, with real before/after examples.
- **Anti-patterns** — what this brand must never do. The most useful page in any
  guideline.

### 5. Ship it twice

Every brand system needs both:

1. **A pack skill** — machine-readable, so future sessions apply it automatically
   without anyone pasting rules.
2. **A human document** — a designed PDF or page the team and client can read.

They must be generated from the same source values so they cannot drift.

---

## Part 2 — Applying a brand system

When producing any asset for a brand that has a pack:

1. **Read the pack first.** Every time. Tokens, voice, anti-patterns, character rules.
2. **Match, don't invent.** Lift exact values from the pack. New work extends the
   existing vocabulary; it does not introduce a parallel one.
3. **Honour the accessibility floor** in the pack (minimum type size, contrast ratio,
   hit target). These are constraints, not preferences, and they outrank aesthetics.
4. **Respect the anti-patterns.** If a design needs one to work, the design is wrong.
5. **Targeted changes stay targeted.** Asked to change a colour, change the colour.
   Suggest broader improvements; don't apply them unasked.

### Craft rules that apply to every brand

- **No filler.** Every element earns its place. Empty space is a composition problem,
  not a prompt to add content.
- **No fabricated facts.** Prices, dates, statistics, addresses and testimonials are
  either real or visibly bracketed as `[PLACEHOLDER]`. Never invent a number.
- **Copy is the product** on marketing surfaces. Specific beats generic. Never lorem
  ipsum, never interchangeable filler that could describe any business.
- **Icons are drawn, never emoji** — unless the brand's pack says emoji are part of it.
- **Flex/grid with `gap`**, not margins and whitespace, for any group of siblings.
- **Avoid AI-design tells:** gradient-mesh backgrounds by default, rounded cards with
  a left accent border, glassmorphism, purple-to-blue gradients, Inter/Roboto by
  default, decorative statistics nobody asked for.
- **Recreate from source, not memory.** When source exists — a repo, a stylesheet, a
  PDF — read it. Screenshots are guidance; source is truth.

### Accessibility floors (defaults, unless the pack raises them)

- Body text 16px minimum on screen, 12pt minimum in print
- Contrast 4.5:1 for body text, 3:1 for large text and meaningful graphics
- Hit targets 44px minimum
- Never carry meaning by colour alone
- Line length 45–75 characters

Raise these when the audience needs it. Older, low-vision, low-literacy or
distressed audiences need larger, plainer, higher-contrast work than a design
portfolio suggests.

---

## Part 3 — Producing the deliverables

- **Visual exploration and design surfaces** → the `design` skill (multi-artboard
  canvas the client can edit directly).
- **Charts, dashboards, any data display** → the `dataviz` skill, with the pack's
  palette substituted.
- **The human-readable guideline document** → the `pdf` skill, generated from the
  pack's values.
- **AI imagery** → generate against the pack's prompt library so output stays
  consistent between sessions and operators.

## Starting a new client

1. Create the client's repo.
2. Copy `.claude/skills/brand-system/` into it unchanged.
3. Create `.claude/skills/<client>-brand/SKILL.md` from `pack-template.md`.
4. Run Part 1.

Client data never crosses repos. The method is the only thing that is shared.
