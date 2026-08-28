# NEO NEEDS LP

ナイトワーク向け SNS運用代行「NEO NEEDS」のランディングページ一式です。

## 公開ページ

- トップ（LP） … `index.html`
- プライバシーポリシー … `privacy.html`
- 特定商取引法に基づく表記 … `tokushoho.html`

## ファイル構成

| ファイル / フォルダ | 内容 |
| --- | --- |
| `index.src.html` | 編集用のソース（人が読める形）。**修正はこちらを直します** |
| `index.html` | 公開用（圧縮済み）。`index.src.html` から生成します |
| `img/` | メンバー写真 |
| `hero.mp4` / `hero-poster.jpg` | ファーストビューの動画とサムネイル |
| `reel-*.mp4` / `reel-*.jpg` | 実績リールの動画とサムネイル |
| `logo*.png` / `favicon*` / `og-*.jpg` | ロゴ・アイコン・SNSシェア用画像 |

## 動かし方（ローカル確認）

このフォルダを丸ごとダウンロードして `index.html` をブラウザで開くだけで表示できます。

サーバーの動作に近い形で確認したい場合は、フォルダ内で次のコマンドを実行し、
ブラウザで `http://localhost:8000` を開いてください。

```bash
python3 -m http.server 8000
```

## 修正するとき

1. `index.src.html` を編集します
2. 次のコマンドで公開用の `index.html` を作り直します

```bash
npx html-minifier-terser index.src.html -o index.html \
  --collapse-whitespace --remove-comments --minify-css --minify-js
```

## サーバーへの設置

静的ファイルのみで動くため、フォルダの中身をそのままWebサーバーへ置けば公開できます
（Netlify・Vercel・GitHub Pages・レンタルサーバー等いずれも可）。
