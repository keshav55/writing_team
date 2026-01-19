# MAP.md — writing_team

> Navigation index for AI agents. Use file:line references.

---

## Quick Search

```bash
# Find all skills
rg "name:" skills/*/SKILL.md

# Find pattern definitions (copy-editor)
rg "###.*\d+\." skills/copy-editor/SKILL.md

# Find checklists
rg "\[ \]" skills/
```

---

## Project Overview

**What:** Three AI agent skills for writing tasks. Plan, write, review.

**Structure:**
```
writing_team/
├── README.md
├── skills/
│   ├── planner/           ← outline, research, structure
│   │   ├── README.md
│   │   └── SKILL.md
│   ├── writer/            ← draft with voice
│   │   ├── README.md
│   │   └── SKILL.md
│   └── copy-editor/       ← review, fix AI patterns
│       ├── README.md
│       └── SKILL.md
└── atris/
```

---

## Workflow

```
planner → writer → copy-editor
 (what)   (draft)   (review)
```

---

## Skills

| Skill | Location | Triggers |
|-------|----------|----------|
| planner | `skills/planner/SKILL.md` | plan this, outline, research |
| writer | `skills/writer/SKILL.md` | write this, draft this |
| copy-editor | `skills/copy-editor/SKILL.md` | copy edit, review writing |

---

## Skill Internals

### planner

| Section | Location |
|---------|----------|
| Frontmatter | `skills/planner/SKILL.md:1-9` |
| Goal Clarification | `skills/planner/SKILL.md:25-33` |
| Audience Analysis | `skills/planner/SKILL.md:35-42` |
| Research Gathering | `skills/planner/SKILL.md:44-59` |
| Outline Creation | `skills/planner/SKILL.md:61-85` |
| Voice Definition | `skills/planner/SKILL.md:87-96` |
| Output Format | `skills/planner/SKILL.md:100-120` |

### writer

| Section | Location |
|---------|----------|
| Frontmatter | `skills/writer/SKILL.md:1-9` |
| Voice Over Correctness | `skills/writer/SKILL.md:25-40` |
| Rhythm Is Structure | `skills/writer/SKILL.md:42-55` |
| Specificity | `skills/writer/SKILL.md:57-72` |
| Openings | `skills/writer/SKILL.md:74-88` |
| Endings | `skills/writer/SKILL.md:90-100` |
| Process | `skills/writer/SKILL.md:104-140` |

### copy-editor

| Section | Location |
|---------|----------|
| Frontmatter | `skills/copy-editor/SKILL.md:1-11` |
| Personality & Soul | `skills/copy-editor/SKILL.md:29-59` |
| Content Patterns (1-6) | `skills/copy-editor/SKILL.md:63-146` |
| Language Patterns (7-12) | `skills/copy-editor/SKILL.md:149-224` |
| Style Patterns (13-18) | `skills/copy-editor/SKILL.md:227-304` |
| Communication Patterns (19-21) | `skills/copy-editor/SKILL.md:307-346` |
| Filler & Hedging (22-24) | `skills/copy-editor/SKILL.md:349-384` |
| Rhythm Patterns (25) | `skills/copy-editor/SKILL.md:387-400` |
| Pre-publish Checklist | `skills/copy-editor/SKILL.md:428-446` |

---

## Critical Files

| File | Purpose |
|------|---------|
| ⭐ `skills/planner/SKILL.md` | Outline and research skill |
| ⭐ `skills/writer/SKILL.md` | Drafting skill with voice principles |
| ⭐ `skills/copy-editor/SKILL.md` | 25 AI patterns + checklist |
| `README.md` | Project overview, installation |

---

## By Concern

### Installation
- Full team: `README.md:49-52`
- Single skill: `README.md:54-58`
- Claude Code path: `~/.claude/skills/`
- Codex path: `~/.codex/skills/`

### Triggers
- planner: "plan this", "outline", "help me plan"
- writer: "write this", "draft this", "start writing"
- copy-editor: "copy edit", "review my writing", "humanize"
