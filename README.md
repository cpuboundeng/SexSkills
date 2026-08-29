# Sex Skills

A curated collection of **[Agent Skills](https://agentskills.io/specification)** for writing adult fiction, erotica, and roleplay (smut/RP).

These skills give AI coding agents — and human writers — a deep, structured reference library covering the craft of sex writing: anatomy, technique, sensation, psychology, power dynamics, vocabulary, and scene structure. Each skill is a self-contained guide that loads on demand when the agent's task matches its description.

> **⚠️ Content warning — adults only (18+).** This repository contains explicit sexual content intended for fiction writing. Everything here depicts **fictional, consenting adults**. Some skills cover taboo or kink themes (incest, CNC, BDSM, breeding, etc.) strictly as **storytelling material**, grounded in consent and safety. If you're under 18, or this content is not for you, please leave.

---

## What Are These?

Agent Skills are the standard format for giving AI agents specialized, on-demand knowledge. A skill is a folder containing a `SKILL.md` file with:

1. **YAML frontmatter** — a `name` and a `description` (the description tells the agent *when* to load the skill).
2. **Markdown body** — the actual reference content (techniques, vocabulary, scene structure, etc.).
3. **Optional `references/`** — deeper material loaded only when needed (used by `bdsm`, `sex`, `anal`, `fingering`, `cum-play`, and more).

The agent sees only the name + description in its context until a task matches, then loads the full guide. This is *progressive disclosure* — 31 rich guides without bloating the prompt.

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
| `skill-style-guide` | The **master craft guide** — POV, pacing, tension, sensory language, consent framing, avoiding clichés, scene structure. Load alongside any act-specific skill. |
| `aftercare` | Emotional and sensory aftercare — cuddling, pillow talk, vulnerability, tenderness, and the charged quiet after sex. |
| `anal` | Complete anal play — preparation, toys, positions, prostate stimulation, butt plugs, anal sex, and pegging (strap-on penetration) for all bodies. |
| `bdsm` | Negotiation, safewords, bondage, D/s, sadism/masochism, impact play, shibari, humiliation, CNC, orgasm control, and more. |
| `blowjob` | Fellatio — giving techniques, receiving sensations, positions, face-fuck dynamics. |
| `breast-play` | Breast and nipple play — breast worship, nipple stimulation, nipple orgasm, titfucking (mammary intercourse). |
| `character-creation` | Creating smut characters — gender & sexuality, race & ethnicity, body type, appearance, personality, preferences, kinks, and backstory. |
| `climax` | Writing the orgasm beat — male/female differences, sensory language, POV, avoiding clichés. |
| `cuckold-cuckquean` | Cuckold/cuckquean dynamics — roles, humiliation, power exchange, scenario variations. |
| `cum-play` | Where the climax lands — creampie/breeding (internal), cumshot (external/facial), bukkake (group facial), plus lactation/milking; the where-to-finish decision, aftermath, power dynamics. |
| `cunnilingus` | Oral sex on a woman — clitoral anatomy, tongue techniques, positions, rhythm, sensory detail, and facesitting. |
| `erotic-massage` | Swedish, sensual, tantric, and nuru massage — oil/touch protocols, the relaxation-to-arousal arc. |
| `exhibitionism-voyeurism` | The gaze — exhibitionism (being seen, public nudity, public sex) and voyeurism (watching, peeping); the watcher/watched dynamic, consent frames. |
| `fingering` | Digital stimulation — external/internal techniques, giver mechanics, receiver sensations, and fisting (whole-hand penetration). |
| `foreplay` | The anticipation arc — teasing, escalation, erogenous zones, building arousal before penetration. |
| `group-sex` | Multi-partner sex — threesomes, foursomes, orgies, swinging, gangbangs, free-use, and double penetration; positions, dynamics, etiquette. |
| `handjob` | Manual stimulation of a penis — grip, lube, strokes, frenulum focus, edging, ruined orgasms. |
| `harem` | Harem and reverse-harem dynamics — archetypes, character types, relationship structures. |
| `incest` | Step-family and blood-relation dynamics — relationship types, family sex (group scenes), tropes, psychology, writing techniques. |
| `infidelity` | Infidelity & cheating — the affair, secrecy, guilt, discovery, and NTR (netorare) as its anguished genre cousin. |
| `kissing` | The kissing guide — Kama Sutra types to modern styles, techniques, sensory detail. |
| `lesbian-gay` | Queer sex dynamics — butch/femme roles, top/bottom identities, intimacy styles, techniques. |
| `masturbation` | Self-pleasure for male/female anatomy — techniques, sensations, positions, edging. |
| `monster-tentacle` | Monster and tentacle erotica — teratophilia, monsterfucking, tentacles, knotting, oviposition, non-human anatomy in fantasy smut. |
| `roleplay` | Scripted fantasy scenarios — personas, power dynamics, the in-character arc. |
| `seduction` | The pre-desire phase — first meeting, the spark, flirting/banter, the push-pull, pursuit and the chase, the threshold where intent becomes unambiguous. |
| `sex` | Sex scenes — 24 types (romantic, casual, angry, first-time, quickie…) + positions, sensations, dynamics. |
| `sex-toys` | Vibrators, air-pulse toys, dildos, anal toys, strokers, cock rings, remote-controlled/public play; materials, lube, safety. |
| `squirting` | Female ejaculation — the G-spot and Skene's glands, technique, sensation, writing the release. |
| `verbal-erotica` | Verbal erotica — spoken dirty talk (praise, degradation, commands, begging) and sexting/phone sex; tone calibration, pacing exchanges. |
| `watersports` | Watersports — golden showers, piss play, urolagnia, omorashi (desperation/wetting); the intimacy/degradation spectrum of urine in sex. |

---

## Repository Structure

```
SexSkills/
├── README.md                  # You are here
├── TEMPLATE_NEW_SKILL.md      # Guide for adding a new skill
├── .agents/
│   └── skills/                # ← The skills (31 directories)
│       ├── AFTERCARE/SKILL.md
│       ├── ANAL/
│       │   ├── SKILL.md
│       │   └── references/    # pegging
│       ├── BDSM/
│       │   ├── SKILL.md
│       │   └── references/    # 31 sub-guides loaded on demand
│       ├── BREAST_PLAY/SKILL.md
│       ├── CHARACTER_CREATION/
│       │   ├── SKILL.md
│       │   └── references/    # gender/sexuality, race/ethnicity, body type, appearance, personality/backstory, preferences, kinks
│       ├── CUM_PLAY/
│       │   ├── SKILL.md
│       │   └── references/    # creampie/breeding, cumshot, bukkake, lactation
│       ├── CUNNILINGUS/
│       │   ├── SKILL.md
│       │   └── references/    # facesitting
│       ├── EXHIBITIONISM_VOYEURISM/
│       │   ├── SKILL.md
│       │   └── references/    # public nudity/exhibitionism, voyeurism
│       ├── FINGERING/
│       │   ├── SKILL.md
│       │   └── references/    # fisting
│       ├── GROUP_SEX/
│       │   ├── SKILL.md
│       │   └── references/    # threesome, gangbang/free-use, double penetration
│       ├── INCEST/
│       │   ├── SKILL.md
│       │   └── references/    # family sex
│       ├── INFIDELITY/
│       │   ├── SKILL.md
│       │   └── references/    # ntr
│       ├── MONSTER_TENTACLE/SKILL.md
│       ├── SEDUCTION/SKILL.md
│       ├── SEX/
│       │   ├── SKILL.md
│       │   └── references/    # types + positions
│       ├── SEX_TOYS/
│       │   ├── SKILL.md
│       │   └── references/    # remote-controlled & public play
│       ├── VERBAL_EROTICA/
│       │   ├── SKILL.md
│       │   └── references/    # dirty talk, sexting
│       ├── WATERSPORTS/SKILL.md
│       └── ... (13 more)
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
