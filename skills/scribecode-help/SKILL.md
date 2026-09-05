---
name: scribecode-help
description: >
  (scribecode) Show a concise reference for ScribeCode commands and its
  feature-by-feature workflow. Trigger for /scribecode-help or questions about
  how to use ScribeCode.
---

# ScribeCode quick reference

| Command | What it does |
| --- | --- |
| `/scribecode` | Start ScribeCode mode. |
| `/scribecode off` | Return to normal mode. |
| `/scribecode-help` | Show this reference. |

ScribeCode inspects the project and writes one concise feature doc at a time to `.scribedocs/`. Each doc gives exact file locations, copyable code blocks or focused diffs, a runnable check, and a production-style commit message.

The workflow follows working product slices rather than architectural tasks: build something visible or usable now, verify it, commit it, then choose the next slice. Utilities and abstractions appear only when the current feature needs them.

Before setup or integration work, ScribeCode checks the current official quickstart and prefers the framework or package CLI. It gives you the normal scaffold/install command instead of rebuilding generated `package.json`, TypeScript, or framework configuration by hand.

The user types the implementation. Say `done`, `next`, or `.` when the current slice works; if it fails, share the error and ScribeCode will revise the current instructions.

Only the current slice is fully authored. If you ask for advance planning, ScribeCode may add up to four short future specs without locking in code, filenames, or symbol names; it revises those specs when your implementation changes the assumptions behind them.

If you question or change an instruction, ScribeCode answers your concern first and does not assume you implemented the change. When you move on, it checks the actual project, rewrites affected docs to match your decisions, and then updates any cascading future specs.

Doc numbers stay local. They never appear in source comments, product text, or commit messages.

For a tiny cosmetic fix, ScribeCode asks whether to write a short doc or apply the fix directly.
