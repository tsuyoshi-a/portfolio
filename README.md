# Tsuyoshi A. — サイト（CSS埋め込み版）

CSSとJavaScriptを各HTMLファイルの中に直接書き込んであります。
**HTMLファイルを置くだけでデザインが反映されます**（cssフォルダ・jsフォルダは不要）。

## GitHubへのアップロード手順

1. リポジトリ `tsuyoshi-a.github.io` を開く
2. 「Add file」→「Upload files」
3. **6つのHTMLファイルをまとめてドラッグ&ドロップ**
   - index.html / about.html / discography.html / news.html / works.html / contact.html
4. 下の「Commit changes」をクリック

古い `css` フォルダや `js` フォルダが残っていても問題ありませんが、
気になる場合は消してかまいません。

## 画像について

画像はまだ入っていません。HTMLの中で以下のパスを参照しています。

- `images/hero/hero.jpg` … トップの背景画像
- `images/artwork/◯◯.jpg` … ジャケット画像（正方形）
- `images/gear/◯◯.jpg` … 機材写真

GitHub上で `images` フォルダを作って画像をアップすれば表示されます。
（Upload files の画面で、フォルダごとドラッグ&ドロップするのが簡単です）

画像が無い間は、その部分が暗いグレーのタイルになります。レイアウトは崩れません。

## 内容を書き換えるとき

GitHub上でファイル名をクリック → 右上の鉛筆アイコン（Edit）で直接編集できます。
編集したら下の「Commit changes」を押せば反映されます。

- ニュース追加 → news.html の `<article class="news-item">` をコピー
- リリース追加 → discography.html の `<article class="release">` をコピー
- works追加 → works.html の `<li>` をコピー

各ファイルに `<!-- ▼ ... -->` のコメントで目印を入れてあります。

## 色を変えたいとき

各HTMLの `<style>` の中、先頭にある `:root { ... }` を書き換えてください。
6ファイル全部を同じように直す必要があります。

| 変数 | 用途 | 現在の値 |
|---|---|---|
| `--bg` | ページ背景 | `#1f1d1c` |
| `--band` | ヘッダー・フッターの帯 | `#2e2c2b` |
| `--accent` | 緑のボタン | `#4e7c63` |
