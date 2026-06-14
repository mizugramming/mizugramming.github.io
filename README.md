# mizugramming.github.io

GitHub Pages で公開する個人ポートフォリオサイトの雛形です。

想定URL:

```txt
https://mizugramming.github.io
```

## ローカル起動

依存関係をインストールします。

```sh
npm install
```

開発サーバーを起動します。

```sh
npm run dev
```

ビルドを確認します。

```sh
npm run build
```

ビルド結果をローカルで確認します。

```sh
npm run preview
```

## ページ構成

- `/` Home
- `/projects` Projects
- `/research` Research
- `/notes` Notes
- `/gallery` Gallery
- `/about` About

## 今後追加する内容メモ

- Home に名前、短い自己紹介、代表プロジェクトへの導線を追加する
- Projects に Baseball Simulation Lab、Batter Intent Optimization などの詳細ページを追加する
- Research に Simulation、Optimization、Sports Analytics の研究メモを整理する
- Notes に学習メモや技術記事を追加する
- Gallery に GIF、シミュレーション結果、グラフ画像を追加する
- About に自己紹介、技術スタック、GitHub以外のリンクを追加する

画像は `public/assets/images/`、GIF は `public/assets/gifs/` に置く想定です。

## GitHub Pages メモ

ユーザーサイトとして `mizugramming.github.io` リポジトリに配置する想定なので、`astro.config.mjs` の `site` は以下にしています。

```js
site: "https://mizugramming.github.io"
```

別名リポジトリで公開する場合は、Astro の `base` 設定が必要になることがあります。

`.github/workflows/deploy.yml` には GitHub Pages 用の最小 workflow を入れています。
GitHub 側の Pages 設定で Source を `GitHub Actions` にすると、`main` ブランチへの push で公開できます。
