# writing_team

Not one AI writer. A writing team.

A collection of Claude Code skills for writing tasks. Each skill does one job well.

## Skills

| Skill | Purpose | Status |
|-------|---------|--------|
| [copy-editor](skills/copy-editor/) | Detect and fix AI writing patterns | Ready |
| drafter | Generate first drafts with voice | Planned |
| researcher | Outline and gather sources | Planned |
| reviewer | Final pass, fact-check | Planned |

## Installation

```bash
git clone https://github.com/YOUR_USERNAME/writing_team.git ~/.claude/skills/writing_team
```

Or install individual skills:

```bash
cp skills/copy-editor/SKILL.md ~/.claude/skills/copy-editor/SKILL.md
```

## How it works

Each skill is independent. Use one or chain them:

```
researcher → drafter → copy-editor → reviewer
   (outline)   (draft)    (clean)     (verify)
```

Or just use copy-editor on existing text.

## Why

LLMs write slop by default. Statistical patterns that feel safe but read fake.

These skills encode what good writing actually looks like, pattern by pattern, so you can catch the AI tells before publishing.

## Contributing

Add skills to `skills/[name]/SKILL.md`. Each skill needs:
- Clear single purpose
- Before/after examples
- Checklist for validation
