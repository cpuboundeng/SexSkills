# Sex Skills Template

Use this template to create new sex skill directories. Each skill follows the `NAME/SKILL.md` structure.

## Directory Structure

```
sex_skills/
└── <SKILL_NAME>/
    └── SKILL.md
```

## Steps to Create a New Skill

### 1. Create the directory

```bash
mkdir -p sex_skills/<SKILL_NAME>
```

### 2. Create SKILL.md with the YAML frontmatter header

The header must contain `name` and `description` fields:

```yaml
---
name: <skill-name-lowercase>
description: <Brief summary of what the skill covers. Use when ...>
---
```

- **name**: lowercase, hyphenated or single word (no spaces)
- **description**: One-line summary of scope, ending with the trigger context ("Use when the user wants/needs/desires...")

### 3. Write the content

Use the BLOWJOB skill as a reference for structure and depth. Aim to cover:

- **Overview** — What this act/technique is and its erotic appeal
- **Core mechanics** — The how-to: techniques, positions, body parts involved
- **Both perspectives** — What the giver and receiver each experience
- **Variations** — Different styles, power dynamics, moods
- **Writing tips** — Sensory checklist, vocabulary, tone calibration
- **Common pitfalls** — What to avoid and how to fix it
- **Scene structure** — Arc or progression of the act

## Example: BLOWJOB

```
sex_skills/
└── BLOWJOB/
    └── SKILL.md
```

**SKILL.md header:**

```yaml
---
name: blowjob
description: Complete blowjob guide — giving techniques, receiving sensations, positions, and face-fuck dynamics. Use when describing or roleplaying fellatio in smut/RP stories.
---
```

## Naming Conventions

| Field | Convention | Example |
|-------|-----------|---------|
| Directory | UPPERCASE, no spaces | `BLOWJOB`, `FACE_SIT`, `EATING_OUT` |
| name | lowercase, hyphens allowed | `blowjob`, `face-sit`, `eating-out` |
| description | Present tense, scope + trigger | `Complete guide to... Use when...` |

## Quick Copy-Paste Start

```bash
mkdir -p sex_skills/<NAME>

cat > sex_skills/<NAME>/SKILL.md << 'EOF'
---
name: <name>
description: <Description here.>
---

# <Title>

<!-- Your content here -->
EOF
```
