# ScribeCoding

A Claude Code skill that turns Claude into your scribe — you write the code, Claude tells you exactly what to write, where, and why.

## What it is

ScribeCoding flips the usual AI-coding dynamic. Claude is the developer — it knows exactly what to build and why. You are the scribe — your job is to type it out. Claude produces **task docs**: structured markdown guides that tell you exactly what to write, where, and why every line exists. One doc at a time.

You don't paste. You type. You learn the why, not just the what.

## Commands

| Command            | What it does               |
| ------------------ | -------------------------- |
| `/scribecode`      | Activate ScribeCoding mode |
| `/scribecode off`  | Deactivate                 |
| `/scribecode-help` | Quick reference card       |

Natural language also works: `"scribe code"`, `"scribe mode"`, `"be my scribe"`, `"how do i build this step by step"`

Deactivate: `/scribecode off`, `"stop scribe"`, or `"exit scribe mode"`

## Install

```bash
npx skills@latest add tchanwangsa/scribecode
```

## Output

Task docs are written to `.scribedocs/` in your project:

```
.scribedocs/
  data-model/
    01_schema.md
    02_migrations.md
  auth/
    01_middleware.md
    02_token-refresh.md
```

Session history and pattern memory live in `.scribecode/`:

```
.scribecode/
  sessions.log     ← [timestamp]: task, one per line
  patterns.md      ← concepts introduced, with first-seen doc reference
```

## Minor fix behavior

For small cosmetic changes (CSS, text alignment, config tweaks), Claude asks first:

> "Small fix — want a scribedoc or should I just apply it?"

## License

MIT
