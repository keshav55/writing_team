# writing_team

Three skills that work together on writing tasks.

## The idea

One AI writing tool isn't enough. It either drafts (but misses errors) or edits (but can't create). You need a team.

```
planner → writer → copy-editor
 (what)   (draft)   (review)
```

Each skill does one job. Use them alone or chain them together.

## Skills

| Skill | Job | Status |
|-------|-----|--------|
| [planner](skills/planner/) | Outline, research, structure | Ready |
| [writer](skills/writer/) | Draft with voice and rhythm | Ready |
| [copy-editor](skills/copy-editor/) | Review, detect AI patterns, transform | Ready |

## How it works

**Planner** prepares:
- Clarifies the goal
- Analyzes the audience
- Gathers research
- Creates an outline
- Defines the voice

**Writer** drafts:
- Follows the structure
- Writes with voice (sounds human, has opinions)
- Uses specific details
- Varies rhythm
- Flags gaps instead of making things up

**Copy-editor** reviews:
- Detects 26 AI writing patterns
- Rewrites problematic sections
- Checks rhythm (no staccato overcorrection)
- Runs pre-publish checklist
- Transforms slop into human writing

## Installation

**Full team:**
```bash
git clone https://github.com/keshav55/writing_team.git ~/.claude/skills/writing_team
```

**Single skill:**
```bash
mkdir -p ~/.claude/skills/planner
curl -o ~/.claude/skills/planner/SKILL.md https://raw.githubusercontent.com/keshav55/writing_team/master/skills/planner/SKILL.md
```

Works with Claude Code, Codex, Cursor, or any agent that reads skill files.

## Usage

Say the trigger phrase:

| To do this | Say |
|------------|-----|
| Plan a piece | "plan this", "outline", "help me plan" |
| Write a draft | "write this", "draft this", "start writing" |
| Review writing | "copy edit this", "review my writing" |

Or chain them: "Plan, write, and copy-edit a post about X"

## Why this exists

LLMs write slop by default. They pick statistically safe words, hedge everything, and structure text the same way every time.

These skills encode what good writing looks like:
- **Planner** ensures you know what you're writing before you write it
- **Writer** ensures the draft has voice, rhythm, and specifics
- **Copy-editor** catches the AI patterns that slip through anyway

## Contributing

Add or improve a skill:

1. Create or edit `skills/[name]/SKILL.md`
2. Update `skills/[name]/README.md`
3. Submit a PR

Each skill needs:
- Clear single purpose
- Process steps
- Before/after examples
