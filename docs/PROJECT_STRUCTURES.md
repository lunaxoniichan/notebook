---
title: notebook — Project Structure
scope: project
type: architecture
lifecycle: official
status: draft
keywords: [structure, layout, note]
related:
  - docs/SYSTEM_DESIGN.md
updated: 2026-07-30
---

# notebook — Project Structure

> File map / “where is X?”. Architecture lives in [`SYSTEM_DESIGN.md`](SYSTEM_DESIGN.md).

## Layout

```text
notebook/
├── AGENTS.md
├── profile/                 # 公開してよいプロフィール・文体・プライバシー
├── strategy/                # north-star / pillars / monetization memo
├── editorial/               # ネタ帳・カレンダー・会議ログ
├── drafts/                  # 作業中原稿（_template.md）
├── published/               # 公開後メモ（URL・学び）
├── prompts/                 # 編集長 / ライター / 推敲
├── docs/                    # Luna メタ（設計・計画・ワークフロー）
├── .claude/rules/
└── .cursor/rules/
```

## Where to find things

| Concern | Path | Notes |
|---------|------|-------|
| Agent entry | `AGENTS.md` | 編集フロー導線あり |
| Architecture | `docs/SYSTEM_DESIGN.md` | 編集OSの境界 |
| Design spec | `docs/specs/2026-07-30-note-editorial-os-design.md` | 方針ロック |
| 下書きテンプレ | `drafts/_template.md` | 学び締め必須 |
| 進行中原稿 | `drafts/*.md` | status: idea/draft/revise/ready |
| ネタ会議 | `editorial/meetings/` | 1ファイル1回 |
