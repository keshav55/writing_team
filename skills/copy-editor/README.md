# Copy Editor

A Claude Code skill that detects and removes AI writing patterns.

Based on [Wikipedia's Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by WikiProject AI Cleanup.

## Installation

**Claude Code (recommended):**
```bash
git clone https://github.com/YOUR_USERNAME/writing_team.git ~/.claude/skills/writing_team
```

**Manual:**
```bash
cp SKILL.md ~/.claude/skills/copy-editor/SKILL.md
```

## What it detects

**25 patterns across 6 categories:**

| Category | Patterns |
|----------|----------|
| Content | Significance inflation, notability claims, vague attributions |
| Language | AI vocabulary, copula avoidance, synonym cycling |
| Style | Em dashes, boldface overuse, title case |
| Communication | Sycophancy, chatbot artifacts, disclaimers |
| Filler | Hedging, filler phrases, generic conclusions |
| Rhythm | Staccato overcorrection |

## Usage

Invoke in Claude Code:
- "copy edit this"
- "review my writing"
- "make it sound human"

Or paste text and ask for a copy-editor pass.

## Pre-publish checklist

The skill includes a mandatory checklist that catches patterns LLMs miss even when trying to avoid them:

```
[ ] No em dashes anywhere
[ ] No rule of three
[ ] No negative parallelisms
[ ] No AI vocabulary
[ ] No staccato overcorrection
[ ] Sentence lengths vary
[ ] Ending is specific
```

## Part of writing_team

This skill is part of [writing_team](../README.md), a collection of AI writing skills that work together.
