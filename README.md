# SNS観光 ショート動画制作 LP

地方観光施設（ホテル・旅館・グランピング・ダイビングなど）向けの、ショート動画制作サービスの営業LPです。
ビルド不要の静的サイト（プレーンなHTML／JS）。Vercel・GitHub Pages・Netlifyなど、静的ホスティングであればそのまま公開できます。

## ファイル構成

```
index.html          トップページ（LP本体）
contact.html         無料相談・お問い合わせフォーム
support.js           ページを動かすための共通スクリプト（削除・改名しないこと）
thumbs/              動画サムネイル画像
uploads/             紹介動画（mp4）
```

- `index.html` と `contact.html` は素のHTML＋JSで動作し、npm installやビルドコマンドは不要です。
- ページ内の見た目やテキストを直接編集する場合は、HTML中の該当箇所を書き換えてください（`style="..."` はインライン指定です）。
- `support.js` はページ描画に必須のランタイムです。削除するとページが真っ白になります。

## お問い合わせフォームについて

`contact.html` の送信ボタンは、入力内容を件名・本文にまとめた `mailto:` リンクを開く仕組みです（サーバー不要）。
送信先メールアドレスは `contact.html` 内の `after.motion018@gmail.com` を検索すると変更できます。

フォーム送信をメールソフト経由ではなく直接サーバーに送りたい場合は、Formspree・Google フォーム・Vercelのサーバーレス関数などと接続する改修が別途必要です。

## デプロイ（Vercel）

1. このリポジトリをGitHubに作成・push
2. [vercel.com](https://vercel.com) でGitHubアカウント連携 → 「Add New Project」→ このリポジトリを選択
3. Framework Preset は **Other**（そのまま）でOK。Build Command・Output Directoryは空欄のままでデプロイ
4. デプロイ後に発行される `https://xxxx.vercel.app` で公開完了

以後、GitHubの `main` ブランチにpushするたびに、同じURLへ自動で再デプロイされます。

## 独自ドメイン

Vercelのプロジェクト設定 → Domains から追加できます。ドメインの取得は先でも後でも構いません（詳しくはチャットの案内を参照）。
