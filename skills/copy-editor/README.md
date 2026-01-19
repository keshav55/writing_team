# Copy Editor

A skill that reviews written content and fixes problems before publishing.

## What it does

1. **Detects AI patterns** - 25 patterns that flag text as machine-generated (based on Wikipedia's AI Cleanup project)
2. **Checks rhythm** - Catches choppy overcorrection and monotonous sentence structure
3. **Validates before publish** - Mandatory checklist that catches what writers miss

## How it reviews

When you give it content, the copy editor:

```
Read → Identify patterns → Rewrite sections → Check rhythm → Run checklist → Output clean version
```

It doesn't just flag problems. It rewrites them and explains what changed.

## Pattern categories

| Category | What it catches |
|----------|-----------------|
| **Content** | Significance inflation, vague attributions, promotional language |
| **Language** | AI vocabulary (delve, crucial, landscape), copula avoidance, synonym cycling |
| **Style** | Em dashes, boldface overuse, title case, emojis |
| **Communication** | Sycophancy, chatbot artifacts, knowledge disclaimers |
| **Filler** | Hedging, filler phrases, generic positive conclusions |
| **Rhythm** | Staccato overcorrection (too many short fragments) |

## Pre-publish checklist

The skill runs this before approving any output:

```
[ ] No em dashes anywhere
[ ] No rule of three (exactly 3 items in lists)
[ ] No negative parallelisms
[ ] No AI vocabulary
[ ] No staccato overcorrection
[ ] Sentence lengths vary
[ ] At least one specific detail
[ ] Ending is concrete, not generic
```

If anything fails, it rewrites and checks again.

## Installation

**Claude Code:**
```bash
git clone https://github.com/keshav55/writing_team.git ~/.claude/skills/writing_team
```

**Codex:**
```bash
cp SKILL.md ~/.codex/skills/copy-editor/SKILL.md
```

**Manual:**
```bash
mkdir -p ~/.claude/skills/copy-editor
cp SKILL.md ~/.claude/skills/copy-editor/SKILL.md
```

## Usage

Invoke by saying:
- "copy edit this"
- "review my writing"
- "make it sound human"

Or paste content and ask for a copy-editor pass.

## Example

**Before:**
> The new software update serves as a testament to the company's commitment to innovation. Moreover, it provides a seamless, intuitive, and powerful user experience, ensuring that users can accomplish their goals efficiently.

**After:**
> The software update adds batch processing, keyboard shortcuts, and offline mode. Early feedback from beta testers has been positive, with most reporting faster task completion.

**What changed:**
- "serves as a testament" → removed (inflated symbolism)
- "Moreover" → removed (AI vocabulary)
- "seamless, intuitive, and powerful" → specific features (rule of three + promotional)
- Vague claims → concrete details

## Reference

Based on [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by WikiProject AI Cleanup.

## Part of writing_team

This skill is one member of [writing_team](../../README.md). Skills work independently or together.
