# Portfolio Website 編集ガイド

このポートフォリオサイトは [Hugo](https://gohugo.io/) と [Wowchemy (Hugo Academic Theme)](https://wowchemy.com/) を使用して構築されています。

## ローカルでのプレビュー方法

以下のコマンドを実行することで、ローカルサーバーを起動し、ブラウザで変更をリアルタイムに確認できます。

```bash
hugo server -D
```

サーバー起動後、 `http://localhost:1313/` にアクセスしてください。

## 主要なファイルの編集方法

コンテンツは主に `content/` ディレクトリ内の Markdown ファイルを編集することで更新できます。

### 1. 論文・プロジェクト (Achievement / Publication)
- **ファイルパス**: 
  - 日本語: `content/ja/home/publications.md`
  - 英語: `content/en/home/publications.md`
- **編集方法**:
  - `row` クラスで囲まれた HTML ブロックとして記述されています。
  - 新しい項目を追加する場合は、既存の項目をコピー＆ペーストして内容を書き換えてください。
  - 画像は `static/media/publications/` に配置し、パスを `/media/publications/filename.png` のように指定します。

### 2. 職歴 (Experience)
- **ファイルパス**:
  - 日本語: `content/ja/home/experience.md`
  - 英語: `content/en/home/experience.md`
- **編集方法**:
  - YAML 形式で記述されています。 `experience:` セクション以下に項目を追加・削除してください。
  - `title`, `company`, `date_start` は必須項目です。

## 注意事項
- **マルチリンガル対応**: 日本語 (`ja/`) と英語 (`en/`) の両方のファイルを編集することを忘れないでください。
## レイアウトの微調整
- **HTML の使用**: Publication セクションなどはレイアウト調整のために直接 HTML を記述しています。クラス名（例: `text-center`, `col-md-6`）を変更する際は Bootstrap 4 の構文に従ってください。

### Experience セクションの配置調整
Experience セクション全体の表示位置（左右のずらし具合）を調整するには、以下のファイルを編集します。

- **ファイル**: `layouts/partials/widgets/experience.html`
- **箇所**: ファイル冒頭付近（6行目など）の `<div>` タグ内のクラス

```html
<!-- 例: 左側に 42% (5/12) の余白を空け、コンテンツをその右側に配置する場合 -->
<div class="col-12 col-lg-7 offset-lg-5">
```

- `offset-lg-X`: 左側の余白のサイズを指定します。数字 `X` (1〜11) が大きいほど、コンテンツは右に移動します。
- `col-lg-Y`: コンテンツ自体の幅を指定します。数字 `Y` (1〜11) が大きいほど、幅が広がります。
- 基本的に `X + Y = 12` になるように設定すると、右端まで綺麗に収まりますが、調整次第で合計を12未満にすることも可能です。
