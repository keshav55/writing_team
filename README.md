# writing_team

Skills that work together on writing tasks.

## The idea

One AI writing tool isn't enough. It either drafts (but misses errors) or edits (but can't create). You need a team.

Each skill here does one job well. Use them alone or chain them together.

## Skills

| Skill | Job | Status |
|-------|-----|--------|
| [copy-editor](skills/copy-editor/) | Review and fix AI patterns, check rhythm, validate before publish | Ready |
| drafter | Generate first drafts with voice and structure | Planned |
| researcher | Gather sources, build outlines, fact-check claims | Planned |
| reviewer | Final read, consistency check, publish approval | Planned |

## How skills work

A skill is a markdown file that tells an AI agent how to do one task. The format:

```markdown
---
name: skill-name
description: What it does
triggers:
  - words that activate it
---

# Instructions

The actual skill content...
```

When you say a trigger phrase, the agent loads the skill and follows its instructions.

## Installation

**Full team (recommended):**
```bash
git clone https://github.com/keshav55/writing_team.git ~/.claude/skills/writing_team
```

**Single skill:**
```bash
mkdir -p ~/.claude/skills/copy-editor
curl -o ~/.claude/skills/copy-editor/SKILL.md https://raw.githubusercontent.com/keshav55/writing_team/master/skills/copy-editor/SKILL.md
```

Works with Claude Code, Codex, Cursor, or any agent that reads skill files.

## Chaining skills

Use one skill or chain them:

```
researcher → drafter → copy-editor → reviewer
```

Each skill hands off to the next. The copy-editor catches what the drafter missed. The reviewer catches what the copy-editor missed.

## Why this exists

LLMs write slop by default. They pick statistically safe words, hedge everything, and structure text the same way every time. The output is technically correct but obviously fake.

These skills encode what good writing actually looks like. Not rules to memorize, but patterns to detect and fix.

## Contributing

Add a skill:

1. Create `skills/[name]/SKILL.md`
2. Add a `skills/[name]/README.md` explaining what it does
3. Update this README's skill table
4. Submit a PR

Each skill needs:
- Clear single purpose
- Before/after examples
- Checklist for validation
