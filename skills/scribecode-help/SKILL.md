---
name: scribecode-help
description: >
  (scribecode) Quick reference card for ScribeCode commands and workflow.
  Trigger: /scribecode-help, "scribecode help", "what are the scribecode commands",
  "how do I use scribecode".
---

# ScribeCode — Quick Reference

## Commands

| Command            | What it does                                                               |
| ------------------ | -------------------------------------------------------------------------- |
| `/scribecode`      | Activate ScribeCode mode. Claude becomes the developer; you type the code. |
| `/scribecode off`  | Deactivate. Return to normal mode.                                         |
| `/scribecode-help` | This card.                                                                 |

## How it works

1. You say `/scribecode` and describe what you're building
2. Claude asks one message worth of questions (stack, what's scaffolded)
3. Claude produces a **task doc** — exact code, exact location, every line explained
4. You open the doc in one pane, your editor in another. You type it out.
5. You say "done" / "next" / "." when finished
6. Claude produces the next doc

## Output files

```
.scribedocs/
  data-model/
    01_schema.md
    02_migrations.md
  auth/
    01_middleware.md
    02_token-refresh.md

.scribecode/
  sessions.log     ← what's been built so far
  patterns.md      ← concepts introduced (no re-explaining)
```

## What Claude will not do in scribecode mode

- Write implementation files directly
- Hand you a complete file to paste
- Skip lines with `// ...`
- Produce multiple docs at once (unless you ask)
- Write a progress check that just says "run your tests"

## Small fixes

For cosmetic changes (CSS tweaks, config values, renames), Claude asks:

> "Small fix — want a scribedoc or should I just apply it?"

Say "apply it" and Claude handles it directly.

## Deactivate

`/scribecode off` or say "stop scribe" / "exit scribe mode"
