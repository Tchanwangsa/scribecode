# ScribeCode

ScribeCode turns the AI into the developer and you into the scribe: it decides the next small feature slice, gives you the exact code, and you type it into the project.

## How it works

ScribeCode works feature by feature instead of planning the whole repository up front. Each doc should produce something observable now—a working screen, a migration used by the feature, or a request that completes a real path through the app.

Instructions are concise: exact file locations, complete code blocks or focused diffs, a runnable check, and a normal production commit message. There is no line-by-line commentary, and utilities are introduced only when the current feature needs them.

Before scaffolding a project or integrating a tool, ScribeCode checks its current official quickstart and uses the normal generator or CLI command. It does not make beginners reconstruct generated manifests and TypeScript or framework configuration by hand when the ecosystem already provides a supported setup path.

Only the feature being implemented now receives exact code. When advance planning is requested, ScribeCode keeps at most four future slices as general specs without premature symbol names or file-level decisions, then reshapes them around any changes made while typing the current slice.

Questions and requested changes are answered before any planning maintenance. When you finish or move to another doc, ScribeCode checks what you actually implemented, rewrites affected docs to reflect your decisions, and updates downstream specs from the verified project rather than assuming you followed the original instructions.

## Commands

| Command | What it does |
| --- | --- |
| `/scribecode` | Activate ScribeCode mode |
| `/scribecode off` | Deactivate ScribeCode mode |
| `/scribecode-help` | Show the quick reference |

Natural language also works: `scribe code`, `scribe mode`, `be my scribe`, or `build together step by step`.

## Install

```bash
npx skills@latest add tchanwangsa/scribecode
```

## Output

Feature docs are written one at a time:

```text
.scribedocs/
  saved-sessions/
    01_list-sessions.md
    02_open-session.md
```

Optional session memory lives in `.scribecode/`:

```text
.scribecode/
  sessions.log
  patterns.md
```

Doc numbers are local navigation metadata. ScribeCode never puts them—or references to docs, tasks, or ScribeCode—into implementation comments, product text, or commit messages.

## Small fixes

For a cosmetic or tiny quality-of-life change, ScribeCode asks whether you want a short feature doc or want it applied directly.

## License

MIT
