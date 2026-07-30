# notebook — Agent Guide

Canonical agent entry for Cursor and Claude Code.
(`CLAUDE.md` is a symlink to this file.) Keep this file short — project invariants go in
optional `RULES.md`; generic engineering rules live in Luna Agent Kit (`workflow-guide`, `vibe-rules`).

## Instruction priority (highest wins)

1. **User explicit instructions** (direct chat)
2. **Project rules** (`RULES.md` if present, this file, `.claude/rules/` / `.cursor/rules/`)
3. **Plugin skills** (`workflow-guide`, `vibe-rules`, `dev-*`, `review-*`, …)
4. **Default model behavior**

## Read first

| Doc | Role |
|-----|------|
| [`docs/README.md`](docs/README.md) | Doc catalog, ownership rules, read order |
| [`docs/SYSTEM_DESIGN.md`](docs/SYSTEM_DESIGN.md) | Architecture / services / data flow |
| [`docs/PROJECT_STRUCTURES.md`](docs/PROJECT_STRUCTURES.md) | File map / where code lives |
| [`docs/workflows/WORKFLOW.md`](docs/workflows/WORKFLOW.md) | Phase menu + `suggested_skills` |
| [`docs/PLANS.md`](docs/PLANS.md) / [`docs/TODO.md`](docs/TODO.md) | Plan registry / backlog |

Design specs: `docs/specs/` (via `dev-brainstorm`). Plans: `docs/plans/` (via `dev-plan`).

## Development

_(Fill in stack, commands, ports, and env once the project shape is clear.)_

## GitNexus

Run `npx gitnexus analyze` at the repo root before relying on call graphs — do not grep for
callers/callees. Indexes are per-repo.