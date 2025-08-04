このガイドの英語版は、日本語版の後にあります。
This guide is available in English following the Japanese version.

---

# Roo Code 統合仕様駆動開発ワークフロー 実践ガイド

このガイドは、Roo Codeの高度な機能である**カスタムルール**と**モード**を活用し、プロフェッショナルレベルの仕様書をAIとの対話を通じて生成し、実装までをシームレスに行うための、**具体的なステップバイステップの操作手順**を解説します。

## 🎯 目的と主な改善点 (v4)

* **タスク進捗の自動更新:** `Orchestrator`モードを強化し、タスク完了時に`tasks.md`のチェックボックスを自動で`[x]`に更新する機能を追加しました。これにより、タスクリストがリアルタイムの進捗管理ボードとして機能します。

## ⚙️ セットアップ手順

1. **ZIPファイルのダウンロード**: ページ上部のボタンから、すべての設定ファイルをダウンロードします。

2. **プロジェクトルートに展開**: ダウンロードしたZIPファイルを、あなたの開発プロジェクトのルートディレクトリで展開してください。これにより、Roo Codeが認識する`.clinerules/`ディレクトリが作成されます。

3. **プロジェクト概要の編集**: `projectBrief.md`を開き、あなたのプロジェクトに合わせて内容を編集してください。

## 🚀 実行ワークフロー

プロジェクトの状況に応じて、以下の2つのパターンのどちらかを選択して開発を開始します。

### パターンA: 外部仕様書ハンドオフフロー

Roo Codeの外部で作成済みの仕様書を使って実装を開始するケースです。

#### ステップ1: Orchestratorモードの起動

```
/mode orchestrator
```

#### ステップ2: 実装の開始

`tasks.md`のパスを正確に指定します。

```
Execute the plan defined in ./specs/[feature-name]/tasks.md
```

Roo Codeはタスク実行後、自動で`tasks.md`のチェックボックスを更新します。

### パターンB: Roo Code 対話型仕様生成フロー

アイデア段階から開発を始めるケースです。

#### ステップ1: Architectモードの起動

```
/mode spec-architect
```

#### ステップ2: 要件定義・設計・計画と承認

AIのガイドに従い、`requirements.md`, `design.md`, `tasks.md`を作成します。各フェーズの終わりに`要件を承認します`のようなコマンドで承認します。

#### ステップ3: 実装フェーズへの移行

計画承認後、AIの指示に従いモードを切り替えます。

```
/mode orchestrator
```

#### ステップ4: 実装の開始

作成した計画を実行するよう指示します。

```
先ほど作成した計画を実行してください。
```

Roo Codeは実装を開始し、進捗に応じて`tasks.md`を自動更新します。

---
---

# Practical Guide to the Roo Code Integrated Specification-Driven Development Workflow

This guide provides **concrete, step-by-step instructions** for leveraging Roo Code's advanced features—**Custom Rules** and **Modes**—to seamlessly generate professional-level specifications through dialogue with AI and carry through to implementation.

## 🎯 Objective and Key Improvements (v4)

* **Automatic Task Progress Updates:** The `Orchestrator` mode has been enhanced to automatically update checkboxes in `tasks.md` to `[x]` upon task completion. This allows the task list to function as a real-time progress management board.

## ⚙️ Setup Procedure

1. **Download the ZIP File**: Download all configuration files using the button at the top of the page.

2. **Extract to Project Root**: Unzip the downloaded file in the root directory of your development project. This will create the `.clinerules/` directory, which Roo Code recognizes.

3. **Edit the Project Brief**: Open `projectBrief.md` and edit the content to match your project.

## 🚀 Execution Workflow

Choose one of the following two patterns to start development, depending on your project's status.

### Pattern A: External Specification Handoff Flow

Use this flow when you are starting implementation with specifications that have already been created outside of Roo Code.

#### Step 1: Activate Orchestrator Mode

```
/mode orchestrator
```

#### Step 2: Begin Implementation

Specify the exact path to `tasks.md`.

```
Execute the plan defined in ./specs/[feature-name]/tasks.md
```

After executing the tasks, Roo Code will automatically update the checkboxes in `tasks.md`.

### Pattern B: Roo Code Interactive Specification Generation Flow

Use this flow when starting development from the idea stage.

#### Step 1: Activate Architect Mode

```
/mode spec-architect
```

#### Step 2: Define Requirements, Design, Plan, and Approve

Follow the AI's guidance to create `requirements.md`, `design.md`, and `tasks.md`. At the end of each phase, approve it with a command like `I approve the requirements`.

#### Step 3: Transition to the Implementation Phase

After approving the plan, switch modes as instructed by the AI.

```
/mode orchestrator
```

#### Step 4: Begin Implementation

Instruct the AI to execute the plan you just created.

```
Execute the plan we just created.
```

Roo Code will begin implementation and automatically update `tasks.md` as progress is made.
