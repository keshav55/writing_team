# MAP.md — writing_team

> Navigation index for AI agents. Use file:line references.

---

## Quick Search

```bash
# Find a skill
rg "name:" skills/

# Find pattern definitions
rg "###.*\d+\." skills/copy-editor/SKILL.md

# Find checklist
rg "\[ \]" skills/copy-editor/SKILL.md
```

---

## Project Overview

**What:** A collection of AI agent skills for writing tasks. Each skill does one job.

**Structure:**
```
writing_team/
├── README.md                      ← project overview, installation
├── skills/
│   └── copy-editor/
│       ├── README.md              ← skill docs, usage examples
│       └── SKILL.md               ← the actual skill (25 patterns)
└── atris/                         ← workspace (MAP, TODO, logs)
```

---

## By Feature

### Skills

| Skill | Location | Status |
|-------|----------|--------|
| copy-editor | `skills/copy-editor/SKILL.md` | Ready |
| drafter | — | Planned |
| researcher | — | Planned |
| reviewer | — | Planned |

### copy-editor internals

| Section | Location |
|---------|----------|
| Frontmatter (triggers) | `skills/copy-editor/SKILL.md:1-11` |
| Personality & Soul | `skills/copy-editor/SKILL.md:29-59` |
| Content Patterns (1-6) | `skills/copy-editor/SKILL.md:63-146` |
| Language Patterns (7-12) | `skills/copy-editor/SKILL.md:149-224` |
| Style Patterns (13-18) | `skills/copy-editor/SKILL.md:227-304` |
| Communication Patterns (19-21) | `skills/copy-editor/SKILL.md:307-346` |
| Filler & Hedging (22-24) | `skills/copy-editor/SKILL.md:349-384` |
| Rhythm Patterns (25) | `skills/copy-editor/SKILL.md:387-400` |
| Process | `skills/copy-editor/SKILL.md:403-420` |
| Pre-publish Checklist | `skills/copy-editor/SKILL.md:428-446` |

---

## By Concern

### Installation
- Full team install: `README.md:41-44`
- Single skill install: `README.md:46-50`
- Claude Code path: `~/.claude/skills/`
- Codex path: `~/.codex/skills/`

### Skill Format
- Frontmatter spec: `README.md:22-35`
- Trigger system: `README.md:37`

### Contributing
- How to add a skill: `README.md:72-82`

---

## Critical Files

| File | Purpose |
|------|---------|
| ⭐ `skills/copy-editor/SKILL.md` | The main skill, 25 AI patterns |
| `skills/copy-editor/README.md` | Skill documentation |
| `README.md` | Project overview, installation |

---

## Planned Skills

| Skill | Purpose | Dependencies |
|-------|---------|--------------|
| drafter | Generate first drafts with voice | — |
| researcher | Outline, gather sources | — |
| reviewer | Final pass, fact-check | copy-editor |

---

## Workflow

```
researcher → drafter → copy-editor → reviewer
   (plan)     (write)    (clean)      (verify)
```

Skills can be used independently or chained.
