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

実行に必要なのは `index.html` だけです。`share/guitar-tab-compare/` にある画像、PDF、古いHTML、切り出し画像は制作途中の素材です。
