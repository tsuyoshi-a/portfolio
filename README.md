# Tsuyoshi A. — サイト

旧WordPressサイトのデザインを、ビルド不要の静的HTML/CSSで再構築したものです。
そのまま GitHub Pages にアップロードして公開できます。

## ファイル構成

```
.
├── index.html          home
├── about.html          about / gears
├── discography.html    discography
├── news.html           news
├── works.html          works
├── contact.html        contact
├── css/style.css       全ページ共通のデザイン
├── js/main.js          スマホのメニュー開閉
└── images/
    ├── hero/           トップの背景画像
    ├── artwork/        ジャケット画像
    ├── gear/           機材写真
    └── works/          実績用の画像
```

## 最初にやること

### 1. 画像を入れる

現在、画像ファイルは入っていません。以下のフォルダに画像を入れてください。
**HTMLに書かれているファイル名と同じ名前**にすれば、自動的に表示されます。

- `images/hero/hero.jpg` … トップページの背景画像（横長・大きめ推奨）
- `images/artwork/` … ジャケット画像（正方形）。ファイル名は `discography.html` 内の `src=` を参照
- `images/gear/` … 機材写真（正方形にトリミングされます）
- `images/works/` … works ページ用

画像が無い間は、その部分が暗いグレーのタイルとして表示されます（レイアウトは崩れません）。

### 2. リンク先を入れる

- `discography.html` の各「Listen Here」ボタンの `href="#"` を、実際の配信ページURLに変更
- `contact.html` の `your-address@example.com` と各SNSのURLを変更
- `index.html` のヒーロー「listen here 🎧」ボタンのURLを変更

### 3. 内容を更新する

- **お知らせを追加** → `news.html` の `<article class="news-item">` をコピーして一番上に追加
- **リリースを追加** → `discography.html` の `<article class="release">` をコピー
- **機材を追加** → `about.html` の `<article class="gear">` をコピー

各ファイルには `<!-- ▼ ... -->` というコメントで目印を入れてあります。

## GitHub Pages で公開する

1. このフォルダの中身を、リポジトリの**直下**にアップロード（`index.html` がルートにある状態）
2. Settings → Pages
3. Source を「Deploy from a branch」、Branch を `main` / `(root)` にして Save

リポジトリ名を `ユーザー名.github.io` にすると、URLに `/リポジトリ名` が付かなくなります。

## デザインについて

旧サイトの見た目に合わせています。変更したい場合は `css/style.css` の先頭にある
`:root { ... }` の値を書き換えると全ページに反映されます。

| 変数 | 用途 | 現在の値 |
|---|---|---|
| `--bg` | ページ背景 | `#1f1d1c` |
| `--band` | ヘッダー・フッターの帯 | `#2e2c2b` |
| `--accent` | 緑のボタン | `#4e7c63` |
| `--font` | 書体 | Quicksand + Noto Sans JP |

書体は旧サイトに近い丸みのあるゴシック（Quicksand）を使っています。
別の書体にしたい場合は、各HTMLの `<head>` にある Google Fonts のURLと
`--font` の値を書き換えてください。

## SEO まわり（任意）

- 各ページの `<title>` と `<meta name="description">` は設定済みです。新しいページを作るときは必ず書いてください。
- Google Search Console にサイトを登録すると、検索キーワードごとの流入が見られます。
- アクセス解析を入れたい場合は、Google Analytics (GA4) のタグを各HTMLの `</head>` の直前に貼り付けてください。
