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
| Frontmatter | `skills/planner/SKILL.md:1-10` |
| Phase 1: DISCOVER | `skills/planner/SKILL.md:22-56` |
| Phase 2: IDENTIFY GAPS | `skills/planner/SKILL.md:59-89` |
| Phase 3: DO THE RESEARCH | `skills/planner/SKILL.md:92-116` |
| Phase 4: BUILD THE OUTLINE | `skills/planner/SKILL.md:119-150` |
| Outputting the Plan | `skills/planner/SKILL.md:153-187` |
| Examples | `skills/planner/SKILL.md:215-288` |
| Handoff | `skills/planner/SKILL.md:302-314` |

### writer

| Section | Location |
|---------|----------|
| Frontmatter | `skills/writer/SKILL.md:1-10` |
| The Loop | `skills/writer/SKILL.md:22-33` |
| Phase 1: SETUP | `skills/writer/SKILL.md:36-52` |
| Phase 2: OPENING | `skills/writer/SKILL.md:55-93` |
| Phase 3: FILL THE BODY | `skills/writer/SKILL.md:96-140` |
| Phase 4: CLOSING | `skills/writer/SKILL.md:143-169` |
| Key Principles | `skills/writer/SKILL.md:240-293` |
| Handoff | `skills/writer/SKILL.md:308-319` |

### copy-editor

| Section | Location |
|---------|----------|
| Frontmatter | `skills/copy-editor/SKILL.md:1-11` |
| Personality & Soul | `skills/copy-editor/SKILL.md:29-60` |
| Content Patterns (1-6) | `skills/copy-editor/SKILL.md:63-146` |
| Language Patterns (7-12) | `skills/copy-editor/SKILL.md:149-224` |
| Style Patterns (13-18) | `skills/copy-editor/SKILL.md:227-304` |
| Communication Patterns (19-21) | `skills/copy-editor/SKILL.md:307-346` |
| Filler & Hedging (22-24) | `skills/copy-editor/SKILL.md:349-384` |
| Rhythm Patterns (25-26) | `skills/copy-editor/SKILL.md:387-453` |
| Pre-publish Checklist | `skills/copy-editor/SKILL.md:497-527` |

---

## Critical Files

| File | Purpose |
|------|---------|
| ⭐ `skills/planner/SKILL.md` | Outline and research skill |
| ⭐ `skills/writer/SKILL.md` | Drafting skill with voice principles |
| ⭐ `skills/copy-editor/SKILL.md` | 26 AI patterns + checklist |
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
