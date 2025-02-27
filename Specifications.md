# Yosuga Creating Talk ToDo

## 📌 実装予定機能一覧

### 🎯 基本機能
- ToDoリストの作成・編集・削除
- 作業の進行状況をリアルタイムでOBSに表示
- 手動チェックで完了タスクに移動
- 進行中のタスクと前2つ、後1つの工程を表示
- 完了タスクに感想(1行)を追加可能
- 作業の進捗バーを表示
- OBS用HTMLを `Yosuga_Creating_Talk_Todo_OBS.html` に書き出し
- OBS用HTMLのフォント・サイズ・文字色変更可能
- ToDoリストの順番を入れ替え可能（ドラッグ＆ドロップ or 上下矢印ボタン）

### ⏳ 作業ログの記録
- 各工程の作業時間を自動記録（完了時間 or 所要時間を選択可能）
- 作業履歴をWordPressへ投稿（REST APIを使用）
- WordPressの通常投稿に記録

### 🔔 ポモドーロタイマー
- 25分作業＋5分休憩（設定変更可）
- 自動再生 or 手動開始の選択
- BGM再生（作業BGM/休憩BGM 切替、フォルダ内の音楽を再生）
- OBS用HTMLにタイマーを表示（非使用時は非表示）

### 🎨 OBS用アニメーション
- 作業工程の変更時にフェードアニメーション
- OBS用HTMLのスライドアニメーション
- タイマーの休憩開始時にエフェクト追加

### 💾 データ保存
- JSON形式でタスクリストを `TaskListLog/` に保存（最新5件まで保持）
- 作業テンプレートを `TaskTemplates/` に保存（ユーザーが任意の名前で保存可能）
- 設定データをJSONファイルで保存

### ⌨️ キーボードショートカット（デフォルトOFF・ユーザー設定可）
- `Ctrl + Enter` → タスク追加
- `Ctrl + ↓` → 次のタスクへ移動
- `Ctrl + ↑` → 前のタスクに戻る
- `Ctrl + Space` → タスク完了
- `Ctrl + Shift + P` → ポモドーロタイマー開始・停止

### 🎥 YouTube API 連携
- 配信時間の取得
- タスク完了時にタイムスタンプ自動生成
- 配信終了後にWordPress投稿にタイムスタンプリストを追加

### 🛠 設定機能
- OBS表示用HTMLの背景色・透明度を設定
- OBS表示用HTMLのフォント・サイズ・文字色変更
- ポモドーロタイマーのON/OFF
- BGMのランダム再生・固定選択
- JSON設定ファイルを手動編集可能

---

## 🚀 アプリ制作手順

### 1️⃣ 基本構成の設計
- `index.html` → アプリのメイン画面
- `main.js` → アプリのロジック
- `styles.css` → アプリ用CSS
- `Yosuga_Creating_Talk_Todo_OBS.html` → OBS用HTML（タスク表示）
- `Yosuga_Creating_Talk_Todo_OBS.css` → OBS用CSS（カスタマイズ用）
- `TaskListLog/` → JSONデータ（タスクリスト）
- `TaskTemplates/` → JSONデータ（テンプレート）
- `wp-plugin/` → WordPressプラグインの開発ディレクトリ

### 2️⃣ ToDoリストの基本機能実装
- タスクの追加・削除・並び替え
- 現在のタスク表示（前2つ・後1つ）
- JSONファイルにデータ保存・復元

### 3️⃣ OBS用HTML・CSSの生成
- `Yosuga_Creating_Talk_Todo_OBS.html` へのデータ書き出し
- 作業進捗バーの追加
- アニメーションの実装（フェード・スライド）

### 4️⃣ ポモドーロタイマーの実装
- タイマー機能（作業/休憩）
- BGMの再生・切替機能
- OBS画面への表示

### 5️⃣ 作業ログ・YouTube API連携
- 作業時間の記録
- REST APIを使ったWordPress投稿
- YouTube APIを使った配信情報の取得
- タスク完了時のタイムスタンプ記録

### 6️⃣ WordPressプラグイン開発
- `yosuga-todo-plugin.php`（REST APIのカスタムエンドポイント）
- タスク履歴をWordPressの通常投稿に追加

### 7️⃣ UI/UXの改善
- キーボードショートカット機能
- 設定画面の作成
- JSON設定ファイルの適用

### 8️⃣ 最終テスト & GitHub公開
- 動作確認 & デバッグ
- GitHubリポジトリへ `.md` ファイルとコードをアップロード

---

## ✅ 今後の展望
- Twitch API連携（YouTube以外のプラットフォーム対応）
- 作業進捗のリアルタイム共有機能
- モバイル対応（スマホ・タブレットでの操作）

---
