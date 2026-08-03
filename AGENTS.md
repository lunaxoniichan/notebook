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
| [`docs/specs/2026-07-30-note-editorial-os-design.md`](docs/specs/2026-07-30-note-editorial-os-design.md) | note 編集OS設計 |

Design specs: `docs/specs/` (via `dev-brainstorm`). Plans: `docs/plans/` (via `dev-plan`).

## note 編集フロー（コンテンツ作業）

このリポの本体は **markdown 編集資産**（アプリコードなし）。

1. 方針・柱 → `strategy/` + `prompts/editor-in-chief.md`
2. ネタ → `editorial/idea-bank.md` → 会議 `editorial/meetings/`
3. 下書き → `drafts/_template.md` をコピーし `prompts/writer.md` で執筆
4. 推敲 → `prompts/reviser.md`（学び締め・国名非依存・匿名化）
5. 公開後 → `published/` に URL・要約・学びを残す

プロフィール／声／プライバシー: `profile/`。

## Development

コンテンツ作業が中心。アプリの build / test / ports は v1 対象外。

## GitNexus

Run `npx gitnexus analyze` at the repo root before relying on call graphs — do not grep for
callers/callees. Indexes are per-repo. （現状アプリコードなし）
