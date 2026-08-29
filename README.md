# Lesko Help — Brand System

The brand system for Lesko Help, built to be usable from any computer and any
Claude Code session without local installation.

## How it works

Two skills live in `.claude/skills/`, committed to this repo:

| Skill | What it is | Shared? |
|---|---|---|
| `brand-system` | The **method** — how a brand system is built and applied | Yes, identical in every client repo |
| `lesko-brand` | The **pack** — Lesko Help's actual answers | No, only here |

Open this repo in Claude Code anywhere and both load automatically. Nothing to
install, nothing that drifts between machines.

## Layout

```
.claude/skills/brand-system/   the method (+ pack-template.md for new clients)
.claude/skills/lesko-brand/    Lesko Help's brand pack
brand/                         source values and design files
documents/                     human-readable deliverables (PDF guidelines)
```

## Starting another client

1. Create that client's repo.
2. Copy `.claude/skills/brand-system/` into it unchanged.
3. Create `.claude/skills/<client>-brand/SKILL.md` from `pack-template.md`.

Client data never crosses repos. Only the method is shared.
