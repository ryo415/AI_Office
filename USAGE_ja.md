# AI_Office 使い方

このリポジトリは、Personal AI Office の設定と作業メモリです。

Markdown を中心に運用します。ユーザーは基本的に Chief of Staff に話しかけ、Chief of Staff が必要最小限の workflow、agent、skill、template を選びます。

## 基本ルール

最初に `AI_OFFICE.md` を基準にします。

`AI_OFFICE.md` は運用方針、役割の振り分け、ファイル責務、確認が必要な操作を定義します。他のファイルと矛盾した場合は、`AI_OFFICE.md` を正とします。

## 日常の流れ

1. 粗いアイデアは `inbox/` に入れる。
2. Chief of Staff に依頼内容を整理してもらう。
3. 複雑な依頼だけ workflow を使う。
4. 必要な場合だけ補助 agent を使う。
5. 保存、再利用、Notion貼り付け、GitHub issue化を想定する出力には template を使う。
6. 進行中プロジェクトの詳細は `projects/` に保存する。
7. 継続的に参照する好み、意思決定、プロジェクト索引は `memory/` に保存する。

## ディレクトリの責務

| パス | 目的 | 編集するタイミング |
|---|---|---|
| `AI_OFFICE.md` | 全体の運用方針とルーティングルール | システム全体の振る舞いを変えたいとき |
| `README.md` | リポジトリの短い概要 | 外向けの説明を変えたいとき |
| `agents/` | 役割定義 | 役割の責務を明確にしたいとき |
| `workflows/` | 繰り返し使う作業手順 | よく使う進め方を改善したいとき |
| `skills/` | 特定作業の実行ルール | 能力ごとのルールや出力期待を改善したいとき |
| `templates/` | 成果物の型 | 再利用する文書フォーマットが必要なとき |
| `memory/` | 継続的な文脈と索引 | 好み、意思決定、プロフィール、アクティブプロジェクト索引が変わったとき |
| `projects/` | 進行中または計画中のプロジェクト文書 | プロジェクトを作成または更新するとき |
| `inbox/` | 粗いメモや未整理アイデア | まだプロジェクト化するほど固まっていないとき |

## AI_Office への依頼方法

基本的には Chief of Staff に依頼します。

依頼例:

- 「Chief of Staff、この粗いアイデアを小さなプロジェクトにしてください」
- 「この計画のリスクと抜け漏れをレビューしてください」
- 「このツール候補を調査して、どれを選ぶべきか提案してください」
- 「このタスクから GitHub issue の下書きを作ってください」
- 「このメモを Notion に貼りやすい Markdown にしてください」
- 「この変更を踏まえて active project index を更新してください」

小さな質問は Chief of Staff が直接答えます。

大きめの依頼では、Chief of Staff が以下を整理します。

1. 目的
2. 前提
3. 使う workflow
4. 補助 role
5. skill または template
6. 次のアクション

## Workflow の使い分け

| Workflow | 使う場面 | 典型的な出力 |
|---|---|---|
| `workflows/intake.md` | 曖昧な依頼、複数解釈できる依頼 | 整理済み依頼と次に使う workflow |
| `workflows/project-planning.md` | アイデアをプロジェクト化するとき | `templates/project.md` を使った project document |
| `workflows/research.md` | 比較、最新情報、意思決定のための調査 | `templates/research-report.md` を使った research report |
| `workflows/development.md` | コード、設定、デバッグ、技術設計 | 技術計画、変更ファイル、検証手順、GitHub issue draft |
| `workflows/review.md` | 重要な出力、リスク、前提、品質確認 | `templates/review-report.md` を使った review report |
| `workflows/output.md` | Markdown、Notion、GitHub、task list 形式への整形 | template を使ったコピーしやすい出力 |

## Agent の使い分け

| Agent | 使う場面 |
|---|---|
| Chief of Staff | 常に主インターフェース、ルーティング、最終統合を担当 |
| PM | 目的、スコープ、マイルストーン、タスク、ブロッカー、次アクションが必要なとき |
| Researcher | 根拠、比較、出典、最新情報が必要なとき |
| Engineer | コード、設定、デバッグ、技術設計、検証が関わるとき |
| Secretary | メモ、タスクリスト、要約、外部出力向けMarkdownが必要なとき |
| Reviewer | 意思決定、システム、コスト、セキュリティ、プライバシー、公開に影響するとき |

必要最小限の role だけを使います。すべての依頼を全 agent に通す必要はありません。

## よくある運用

### 粗いアイデアを保存する

1. `inbox/ideas.md` に追加するか、`templates/inbox-item.md` から新しいファイルを作る。
2. 最初から整えすぎない。
3. 後で Chief of Staff に、project、task、research、decision、archive のどれにするか判断してもらう。

### プロジェクトを作る

1. Chief of Staff から始める。
2. `workflows/project-planning.md` を使う。
3. `templates/project.md` から `projects/` 配下にプロジェクトファイルを作る。
4. アクティブなプロジェクトなら `memory/active-projects.md` に索引として追加する。

### 意思決定を記録する

1. `templates/decision-log.md` を使う。
2. 継続的に参照する意思決定は `memory/decisions.md` に追加する。
3. 1つの意思決定エントリには1つの判断だけを書く。

### GitHub issue の下書きを作る

1. `templates/github-issue.md` を使う。
2. ユーザーが明示的に承認するまでは Markdown の下書きに留める。
3. 後で issue 化しやすいように、関連ファイルと acceptance criteria を入れる。

### Notion に貼りやすい Markdown を作る

1. `skills/notion-output.md` を使う。
2. 見出しと property 名を安定させる。
3. ユーザーが明示的に承認するまでは Notion には書き込まない。

### 重要な出力をレビューする

1. `workflows/review.md` を使う。
2. 保存するレビューなら `templates/review-report.md` を使う。
3. 重要なリスク、抜けている前提、具体的な修正に集中する。

## 外部操作の方針

このリポジトリは Markdown-first です。外部連携は将来の拡張です。

確認なしでよいこと:

- 要約
- ブレインストーミング
- 計画
- レビュー
- Markdown の下書き作成
- Notion-ready text の作成
- GitHub issue draft の作成

確認が必要なこと:

- Notion への書き込み
- GitHub issue や pull request の作成・更新
- 依頼範囲外の実ファイル編集
- 破壊的コマンドの実行
- メール送信
- カレンダー予定の作成
- コンテンツ公開

## メンテナンス方針

- ファイルは小さく読みやすく保つ。
- 凝った構造より安定した見出しを優先する。
- 同じプロジェクト詳細を `memory/` と `projects/` の両方に重複させない。
- `memory/active-projects.md` は詳細な進捗管理ではなく索引として扱う。
- `projects/` では1プロジェクト1ファイルを基本にする。
- template は再利用しやすい汎用形にする。
- Notion、GitHub、MCP 用フィールドは、Markdown単体でも意味がある場合だけ追加する。

## 週次レビューのすすめ

週に一度、以下を確認します。

1. `memory/active-projects.md` を確認する。
2. `projects/` のアクティブプロジェクトを更新する。
3. 古い inbox item を進めるか archive する。
4. 重要な意思決定を `memory/decisions.md` に追加する。
5. 安定した好みの変化があれば `memory/preferences.md` を更新する。
6. 保存する場合は `templates/weekly-review.md` を使う。

