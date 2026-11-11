# ドキュメント目次

> **状態:** 設計段階（Phase 0 で設計完了・アプリケーションは未実装）

本ディレクトリには、AI Ticket Analyzer と自律開発ループの設計資料を置いています。
全体像は [リポジトリの README](../README.md) を先に読んでください。

## 読む順番（おすすめ）

短時間で要点をつかむ場合は、1〜3 だけで十分です。

| 順 | ドキュメント | 内容 |
|---|---|---|
| 1 | [harness-engineering.md](./harness-engineering.md) | AI エージェントを安全に動かす枠組み（fail closed、S-1〜S-10、SandboxVerifier、上限） |
| 2 | [loop-engineering.md](./loop-engineering.md) | 自律開発ループの工程・状態遷移・停止理由（未完成・設計段階） |
| 3 | [agentic-workflow.md](./agentic-workflow.md) | ChatGPT・Claude Code・人の分業と、PASS / PARTIAL / BLOCKED のレビュー運用 |
| 4 | [context-engineering.md](./context-engineering.md) | AI への情報の渡し方（CLAUDE.md、ADR、引き継ぎ資料） |
| 5 | [evaluation.md](./evaluation.md) | 3 層の評価設計 |
| 6 | [architecture.md](./architecture.md) | アプリケーションの構成 |
| 7 | [requirements.md](./requirements.md) | 要件 |
| 8 | [security.md](./security.md) | セキュリティ設計 |
| 9 | [tech-stack.md](./tech-stack.md) | 技術選定 |
| 10 | [roadmap.md](./roadmap.md) | Phase ごとの計画 |
| 11 | [adr/README.md](./adr/README.md) | 設計判断の記録（ADR） |

## 成熟度の表記

各ドキュメントでは、次の表記で状態を区別しています。

| 表記 | 意味 |
|---|---|
| ✅ 完了 | 作業が完了している（現時点では Phase 0 の設計のみ） |
| 🔄 運用中 | 手動の運用として実践している |
| 📝 設計段階 | 設計済みで、未実装 |
| 💭 構想 | 方向性のみで、詳細設計はこれから |

## 前提

- 扱うデータはすべて架空です。サンプルは [tickets.sample.jsonl](../examples/fixtures/tickets.sample.jsonl) を参照してください。
- ドキュメント内の上限値・コンポーネント名は設計時点のもので、実装時に評価結果をもとに見直します。
