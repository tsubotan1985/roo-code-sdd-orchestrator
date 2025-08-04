# Rule: Task Execution & Implementation Plan Protocol

## Part A: Task Execution (For `task-executor` mode)

`tasks.md`から単一タスクを実行する際は、以下の手順を厳守してください。

1.  **Context Gathering:** `tasks.md`のタスク内容、リンクされた`requirements.md`の要件、`design.md`の関連設計を読み込み、タスクの目的と技術的背景を完全に理解します。
2.  **TDD (Test-Driven Development):** まず、要件を満たすための失敗するテストケースを作成します。
3.  **Implementation:** テストをパスするための最小限のコードを実装します。
4.  **Verification:** すべてのテストがパスし、リンターのエラーがないことを確認します。
5.  **Commit:** Conventional Commits形式（例: `feat(task-3.1): Implement pixel mask application`）で変更をコミットします。

## Part B: Implementation Plan Creation (For `spec-architect` mode)

`design.md`から`tasks.md`を生成する際は、以下の品質基準を満たしてください。

1.  **Granularity:** タスクは、単一のコミットで完了できる程度に細かく分割します。（例: 「データ前処理機能を実装」ではなく、「DataPreprocessorクラスを実装」「.t3paファイル読み込み機能を実装」のように分割）
2.  **Sequencing:** タスクは依存関係を考慮して、論理的な順序で並べます。
3.  **Traceability:** 各タスクまたはタスクグループの末尾に、対応する要件IDを`_要件: 1.4, 9.1, ..._`の形式で**必ず**記載してください。
4.  **Comprehensiveness:** コーディングだけでなく、テスト作成、ドキュメント修正、エラーハンドリングなどもタスクとして含めてください。
