---
title: notebook — Project Structure
scope: project
type: architecture
lifecycle: official
status: draft
keywords: [structure, layout]
related: []
updated: 2026-07-30
---

# notebook — Project Structure

> File map / “where is X?”. Architecture and data flow live in
> [`SYSTEM_DESIGN.md`](SYSTEM_DESIGN.md) — do not duplicate them here.

## Layout

```text
notebook/
├── AGENTS.md                 # agent entry (CLAUDE.md → symlink)
├── docs/
│   ├── README.md             # doc catalog
│   ├── SYSTEM_DESIGN.md      # architecture
│   ├── PROJECT_STRUCTURES.md # this file
│   ├── PLANS.md / TODO.md
│   └── workflows/WORKFLOW.md
├── .claude/rules/            # Claude always-on rules (+ lessons.md)
└── .cursor/rules/            # Cursor mirrors (*.mdc)
```

## Where to find things

| Concern | Path | Notes |
|---------|------|-------|
| Agent entry | `AGENTS.md` | Commands / env once filled |
| Architecture | `docs/SYSTEM_DESIGN.md` | Services / data flow |
| Workflow | `docs/workflows/WORKFLOW.md` | Phase menu |