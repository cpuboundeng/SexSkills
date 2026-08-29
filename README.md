# Sex Skills

A curated collection of **[Agent Skills](https://agentskills.io/specification)** for writing adult fiction, erotica, and roleplay (smut/RP).

These skills give AI coding agents — and human writers — a deep, structured reference library covering the craft of sex writing: anatomy, technique, sensation, psychology, power dynamics, vocabulary, and scene structure. Each skill is a self-contained guide that loads on demand when the agent's task matches its description.

> **⚠️ Content warning — adults only (18+).** This repository contains explicit sexual content intended for fiction writing. Everything here depicts **fictional, consenting adults**. Some skills cover taboo or kink themes (incest, CNC, BDSM, breeding, etc.) strictly as **storytelling material**, grounded in consent and safety. If you're under 18, or this content is not for you, please leave.

---

## What Are These?

Agent Skills are the standard format for giving AI agents specialized, on-demand knowledge. A skill is a folder containing a `SKILL.md` file with:

1. **YAML frontmatter** — a `name` and a `description` (the description tells the agent *when* to load the skill).
2. **Markdown body** — the actual reference content (techniques, vocabulary, scene structure, etc.).
3. **Optional `references/`** — deeper material loaded only when needed (used by `bdsm` and `sex`).

The agent sees only the name + description in its context until a task matches, then loads the full guide. This is *progressive disclosure* — 25 rich guides without bloating the prompt.

---

## Installation

Skills are just files. Copy the `skills` folder (or the whole repo) into your agent's skill directory.

### Pi

```bash
# Global (all projects)
cp -r .agents/skills/* ~/.agents/skills/

# Or per-project: copy into the project's .agents/skills/
```

### Claude Code

```bash
cp -r .agents/skills/* ~/.claude/skills/
```

> Note: the repo already includes a `.claude/skills` symlink for Claude Code.

### OpenAI Codex / other harnesses

Any harness that reads the Agent Skills standard works. Point it at the `.agents/skills/` directory.

### Manual / no agent

The skills are plain Markdown — read them directly as reference material.

---

## The Skills

| Skill | What it covers |
|-------|----------------|
| `aftercare` | Emotional and sensory aftercare — cuddling, pillow talk, vulnerability, tenderness, and the charged quiet after sex. |
| `anal` | Complete anal play — preparation, toys, positions, prostate stimulation, butt plugs, anal sex for all bodies. |
| `bdsm` | Negotiation, safewords, bondage, D/s, sadism/masochism, impact play, shibari, humiliation, CNC, orgasm control, and more. |
| `blowjob` | Fellatio — giving techniques, receiving sensations, positions, face-fuck dynamics. |
| `breeding-creampie` | The creampie act, impregnation fantasy, breeding dirty talk, cum-play aftermath, power dynamics. |
| `bukkake` | Multi-participant facial ejaculation — origins, mechanics, face vs. body focus, power dynamics. |
| `climax` | Writing the orgasm beat — male/female differences, sensory language, POV, avoiding clichés. |
| `cuckold-cuckquean` | Cuckold/cuckquean dynamics — roles, humiliation, power exchange, scenario variations. |
| `cumshot` | External ejaculation — facial/body finishes, the "where to finish" decision, cum-play aftermath. |
| `cunnilingus` | Oral sex on a woman — clitoral anatomy, tongue techniques, positions, rhythm, sensory detail. |
| `dirty-talk` | Verbal eroticism — praise, degradation, commands, questions, moans, tone calibration. |
| `erotic-massage` | Swedish, sensual, tantric, and nuru massage — oil/touch protocols, the relaxation-to-arousal arc. |
| `exhibitionism-public-nudity` | Exhibitionism, nudism, naturism, public nudity — from flashing to nudist culture and public sex. |
| `fingering` | Digital stimulation — external/internal techniques, giver mechanics, receiver sensations. |
| `group-sex` | Multi-partner sex — threesomes, orgies, swinging; positions, dynamics, etiquette. |
| `handjob` | Manual stimulation of a penis — grip, lube, strokes, frenulum focus, edging, ruined orgasms. |
| `harem` | Harem and reverse-harem dynamics — archetypes, character types, relationship structures. |
| `incest` | Step-family and blood-relation dynamics — relationship types, tropes, psychology, writing techniques. |
| `kissing` | The kissing guide — Kama Sutra types to modern styles, techniques, sensory detail. |
| `lesbian-gay` | Queer sex dynamics — butch/femme roles, top/bottom identities, intimacy styles, techniques. |
| `masturbation` | Self-pleasure for male/female anatomy — techniques, sensations, positions, edging. |
| `roleplay` | Scripted fantasy scenarios — personas, power dynamics, the in-character arc. |
| `sex` | Sex scenes — 23 types (romantic, casual, angry, first-time…) + positions, sensations, dynamics. |
| `sex-toys` | Vibrators, air-pulse toys, dildos, anal toys, strokers, cock rings; materials, lube, safety. |
| `threesome` | Three-person scenes — MMF, MFM, MFF, MMM, FFF configurations, choreography, dynamics. |

---

## Repository Structure

```
SexSkills/
├── README.md                  # You are here
├── TEMPLATE_NEW_SKILL.md      # Guide for adding a new skill
├── .agents/
│   └── skills/                # ← The skills (25 directories)
│       ├── AFTERCARE/SKILL.md
│       ├── BDSM/
│       │   ├── SKILL.md
│       │   └── references/    # 31 sub-guides loaded on demand
│       ├── SEX/
│       │   ├── SKILL.md
│       │   └── references/    # types + positions
│       └── ... (22 more)
└── .claude/
    └── skills -> ../.agents/skills   # symlink for Claude Code
```

Each skill directory follows the Agent Skills standard:

- **`SKILL.md`** — required frontmatter (`name`, `description`) + the guide body.
- **`references/`** *(optional)* — deeper docs referenced from `SKILL.md` and loaded only when needed.

---

## How a Skill Is Structured

Every `SKILL.md` follows a consistent shape:

1. **Frontmatter** — `name` (lowercase, hyphenated) and `description` (scope + "Use when…" trigger).
2. **Overview** — what the act/dynamic is and its erotic appeal.
3. **Mechanics & technique** — the how-to, often with giver/receiver perspectives.
4. **Sensory detail & vocabulary** — concrete language for writing the scene.
5. **Writing tips** — tone calibration, pacing, common pitfalls.
6. **Scene structure** — a worked example arc from approach to aftermath.

The goal throughout is **usable, specific craft** — not vague prose. A good skill answers "how do I actually write this well?"

---

## Contributing

1. Read [`TEMPLATE_NEW_SKILL.md`](TEMPLATE_NEW_SKILL.md) for the format.
2. Create a new directory `SKILL_NAME/SKILL.md` (directory `UPPER_SNAKE_CASE`, `name` in lowercase-hyphenated frontmatter).
3. Match the existing depth and structure — see `blowjob` as the reference example.
4. Keep the `description` specific and include a "Use when…" trigger.

**Conventions**

| Field | Convention | Example |
|-------|-----------|---------|
| Directory | `UPPER_SNAKE_CASE` | `BLOWJOB`, `DIRTY_TALK` |
| `name` | lowercase, hyphens allowed | `blowjob`, `dirty-talk` |
| `description` | Scope + trigger | `"…Use when describing or roleplaying…"` |

---

## Content Policy & Disclaimer

- **Fiction only.** These skills are for writing fictional stories and roleplay. Nothing here is a manual for real-world behavior.
- **All depicted characters are adults (18+).** Nothing in this repository involves minors, and nothing should be used to create content involving them.
- **Consent is central.** Skills covering power exchange, degradation, CNC, or taboo themes treat consent and safety as non-negotiable — both in the content and in the writing guidance.
- **Responsible framing.** Real-world safety notes (safe words, flared bases, lube compatibility, STI/pregnancy awareness) are woven in as appropriate.

---

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) — see the [LICENSE](LICENSE) file for the full legal text.

You are free to share (copy and redistribute the material in any medium or format) and adapt (remix, transform, and build upon the material for any purpose, even commercially), as long as you give appropriate credit to the author.
