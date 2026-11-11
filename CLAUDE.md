# CLAUDE.md — AI Engineering Lab

このファイルは、本リポジトリで作業する Claude Code 向けのルールです。
人間向けの説明は [README.md](README.md) を参照してください。

## 1. 目的

架空のチケット（ダミーデータのみ）を LLM で分析する AI Ticket Analyzer と、
その先の自律開発ループを、安全性・評価・費用管理を重視して設計・実装する。
現在は Phase 0（設計）完了段階で、アプリケーションは未実装。

## 2. 参照先

- 全体像: `README.md` / ドキュメント目次: `docs/README.md`
- 要件 `docs/requirements.md` / 構成 `docs/architecture.md` / 技術選定 `docs/tech-stack.md`
- セキュリティ `docs/security.md` / Harness `docs/harness-engineering.md`
- 自律開発ループ `docs/loop-engineering.md` / 評価 `docs/evaluation.md` / ロードマップ `docs/roadmap.md`
- 情報の渡し方 `docs/context-engineering.md` / 分業と判定 `docs/agentic-workflow.md`
- 設計判断: `docs/adr/`

## 3. 設計判断

- 設計判断は ADR に残す。作成 → AI によるレビュー → 開発者の承認の順で確定する。
- ADR の「未確認事項」は確定扱いにしない。
- 設計が固まる前に実装へ進まない。

## 4. 作業ルール

- 作業前に、変更予定ファイルと影響範囲を提示する。
- 担当外のファイルは変更しない。
- 状態を変える作業は、作業単位ごとに分けた作業ディレクトリで行う。
- 追加するファイルは明示的に指定する。
- commit・push・公開・デプロイは、開発者の明示的な指示と承認がある場合だけ行う。
- 実行していないテストを PASS と報告しない。未実施事項は未実施と書く。
- 実装していない機能を、ドキュメントに実装済みと書かない。

## 5. セキュリティ

- 架空のチケットとダミーデータだけを使う。実在の組織・個人・業務のデータを使わない。
- API キー・トークン・パスワード・秘密鍵の内容を読み取らない、出力しない、記録しない。
- 秘密情報はコミットしない（`.env.example` にはダミー値のみ）。
- AI エージェントの実行権限を、設計（`docs/harness-engineering.md`）の範囲を超えて広げない。
- 外部送信・課金を伴う操作は、開発者の事前承認を得る。
