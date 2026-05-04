# Study Portal — manabi-quiz

学習ポータル（資格・受験クイズの統合ハブ）。

## 構成
- 静的サイト（Vanilla HTML/CSS/JS、依存なし）
- Vercelで自動デプロイ（manabi-quiz.vercel.app）
- 各クイズは独立Vercelプロジェクトで、本サイトはリンク集

## 主要ファイル
- `index.html` — トップ・カードグリッド
- `.github/workflows/claude.yml` — Claude Code GitHub Action

## クイズ追加時のルール
1. カテゴリセクション（💼/💻/🎓 etc.）の `.grid` に `<a class="card card-XXX">` を追加
2. ヘッダー `.stats` の問題数・カテゴリ数を更新
3. `<style>` 内に `.card-XXX { --accent-card: #...; --accent-card2: #...; }` を追記

## Claudeへの依頼の仕方
Issueに `@claude ◯◯のクイズリンクを追加して` で発火。
