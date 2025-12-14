# AI Diet Tracker (AI食事記録アプリ)

AIを活用して食事の写真からカロリーとPFC（タンパク質・脂質・炭水化物）を自動計算・記録するWebアプリケーションです。

## 📱 機能 (Features)

- **AI食事記録**: 写真を撮る/アップロードするだけで、Gemini AIが栄養素を解析。
- **ダッシュボード**: 今日の摂取カロリーとマクロ栄養素の進捗をリンググラフで可視化。
- **体重管理**: 体重と体脂肪率を記録し、推移グラフを自動生成。
- **データ保存**: ブラウザのローカルストレージにデータを安全に保存（リロードしても消えません）。
- **PWAライクなデザイン**: モバイルファーストのGlassmorphismデザイン。

## 🚀 始め方 (Getting Started)

### 1. リポジトリのクローン
```bash
git clone https://github.com/YOUR_USERNAME/diet-tracker.git
cd diet-tracker
```

### 2. 依存関係のインストール
```bash
npm install
```

### 3. 環境変数の設定
プロジェクトのルートに `.env.local` ファイルを作成し、Gemini APIキーを設定してください。
（AI機能を有効にするために必須です）

```env
NEXT_PUBLIC_GEMINI_API_KEY=あなたのGemini_APIキー
```
> **注意**: `NEXT_PUBLIC_` プレフィックスがついているため、このキーはブラウザ側で使用されます。GitHubなどの公開リポジトリには絶対に `.env.local` をコミットしないでください（.gitignoreで除外設定済みです）。

### 4. 開発サーバーの起動
```bash
npm run dev
```
ブラウザで `http://localhost:3000` を開きます。

## 📦 静的ビルド (Static Export)
GitHub PagesなどにデプロイするためのHTMLファイルを生成する場合：

```bash
npm run build
```
`out/` フォルダにHTML/CSS/JS一式が出力されます。

## 🛠️ 技術スタック
- Framework: Next.js 15 (App Router)
- Styling: Vanilla CSS (Custom Design System)
- Icons: Lucide React
- AI: Google Gemini API (gemini-1.5-flash)

## ライセンス
This project is open source.
