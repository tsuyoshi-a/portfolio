# Tsuyoshi A. — Portfolio Site

Tsuyoshi A. のポートフォリオサイトです。ビルド不要の静的 HTML/CSS/JS で構成しているので、そのまま GitHub Pages で公開できます。

## 構成

```
.
├── index.html          # Home
├── about.html           # About & Gear
├── discography.html     # Discography
├── news.html             # News
├── contact.html          # Contact
├── css/style.css
└── js/main.js
```

## GitHub Pages での公開方法

1. このフォルダの中身をリポジトリの直下（ルート）にそのままコミット＆プッシュします。
2. GitHub のリポジトリページで **Settings → Pages** を開きます。
3. "Build and deployment" の Source を **Deploy from a branch** に設定します。
4. Branch を公開したいブランチ（例: `main`）、フォルダを **/ (root)** に設定して Save します。
5. 数分後、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます。

## 編集ポイント

- **テキスト**: 各 `.html` 内の本文（プロフィール、機材、作品情報、ニュース、SNSリンク）はすべてプレースホルダーです。ご自身の内容に差し替えてください。
- **連絡先**: `contact.html` 内の `contact@example.com` を実際のメールアドレスに変更してください（mailto 送信のため）。
- **配色・書体**: `css/style.css` の先頭 `:root` 内にカラーとフォントの変数をまとめています。ここを変更すると全ページに反映されます。
- **ジャケット画像など**: 現状は SVG の等高線モチーフで代用しています。実際の写真・ジャケット画像に差し替える場合は `.release-art` / `.portrait-mark` 内の `<svg>` を `<img>` に置き換えてください。

## デザインについて

自然をモチーフにしたダークミニマルなトーンでまとめています。背景に等高線（コンター）のようなラインを控えめに配置し、見出しには温かみのあるセリフ書体 Fraunces、本文には Work Sans を使用しています。アクセントカラーは琥珀色（`#c89b5c`）です。
