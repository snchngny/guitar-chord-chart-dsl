# Guitar Chord Chart DSL

ギターコード表をDSLから描画する単体HTMLツールです。

## 使い方

`index.html` をブラウザで開くだけで使えます。外部ライブラリや別ファイルは不要です。

- `Default`: 保存済みのデフォルトDSLを読み込みます。未保存の場合はHTML内に埋め込まれたデフォルトDSLを読み込みます。
- `Set`: 現在のDSLをこのブラウザのデフォルトとして保存します。
- `Flip`: 表頭と表側を入れ替えます。`section:` は反転後も列間の縦見出しとして保持されます。
- `Save`: 現在のDSLを `.dsl` として保存します。
- `SVG`: 表をSVGとして保存します。
- `PDF`: ブラウザの印刷機能からPDF保存します。

編集内容はブラウザの `localStorage` に保存されます。別PCへ渡す場合は `index.html` だけでツール本体は動きますが、編集済みDSLを残したい場合は `Save` で `.dsl` も保存してください。

## 配布物

実行に必要なのは `index.html` だけです。

## Web公開

Cloudflare PagesのGit連携で、GitHubの `main` へのpushを自動公開します。

| 設定 | 値 |
| --- | --- |
| Framework preset | None |
| Production branch | `main` |
| Root directory | リポジトリ直下（空欄） |
| Build command | `mkdir -p dist && cp index.html dist/index.html` |
| Build output directory | `dist` |

公開対象は `dist/index.html` のみです。READMEやローカルの保存データはサイトへ配信しません。GitHubのコード更新後、Cloudflareのデプロイ成功を確認してください。

編集内容・デフォルト設定は利用中のブラウザだけに保存され、サーバーへの送信や端末間同期はありません。ローカルHTMLからWeb版へ移る場合も自動では引き継がれないため、必要なDSLは先に `Save` で保存してください。

設定手順は [Cloudflare PagesのGit連携](https://developers.cloudflare.com/pages/configuration/git-integration/) を参照してください。
