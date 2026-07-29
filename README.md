# motion-hook｜ショート動画制作LP

ビルド不要の静的サイトです。このフォルダの中身をそのままサーバー／ホスティングにアップロードすれば公開できます。

## ファイル構成

```
index.html              トップページ（LP本体）
無料相談.dc.html          無料相談・お問い合わせフォーム
プライバシーポリシー.dc.html
利用規約.dc.html
support.js              ページ描画に必須のスクリプト（削除・改名しないこと）
favicon.png             ファビコン
vercel.json             Vercel用設定（他のホスティングでは不要）
thumbs/                 動画サムネイル画像
uploads/                掲載動画（mp4）
```

## アップロード時の注意

- **フォルダ構成をそのまま維持してください。** `thumbs/` と `uploads/` を分けたまま、index.html と同じ階層に置きます。
- `support.js` が無い、または階層がズレると **ページが真っ白になります**。
- トップページは必ず `index.html` という名前のまま、公開ディレクトリの直下に置いてください。
- 日本語ファイル名のページ（無料相談など）もそのままアップロードしてください。名前を変えるとリンク切れになります。

## 問い合わせフォーム

`無料相談.dc.html` の送信ボタンは、入力内容をまとめて `mailto:` を開く仕組みです（サーバー不要）。
送信先は同ファイル内の `after.motion018@gmail.com` を書き換えると変更できます。

## デプロイ（Vercel の場合）

1. このフォルダをGitHubにpush
2. vercel.com →「Add New Project」→ リポジトリを選択
3. Framework Preset は **Other**、Build Command・Output Directory は空欄のままデプロイ
