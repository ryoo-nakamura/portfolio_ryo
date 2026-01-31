# ウェブサイトのカスタマイズ実装計画

ポートフォリオサイトのPublicationセクションの画像を中央揃えにし、Experienceセクションから画像を削除します。また、今後の編集に役立つ README.md を作成します。

## 提案される変更点

### Content (Publications)

#### [MODIFY] [publications.md (ja)](file:///Users/nakamura/Downloads/codes/portfolio_ryo/content/ja/home/publications.md)
#### [MODIFY] [publications.md (en)](file:///Users/nakamura/Downloads/codes/portfolio_ryo/content/en/home/publications.md)

1.  **画像の中央揃え**:
    - 各画像コンテナの `col-md-6` に `text-center` クラスを追加します。
    - 画像タグのスタイルに `display: inline-block;` (または `mx-auto d-block`) を適用し、確実に中央に配置されるようにします。

### Content (Experience)

#### [MODIFY] [experience.md (ja)](file:///Users/nakamura/Downloads/codes/portfolio_ryo/content/ja/home/experience.md)
#### [MODIFY] [experience.md (en)](file:///Users/nakamura/Downloads/codes/portfolio_ryo/content/en/home/experience.md)

1.  **画像の削除**:
    - 各職歴項目の `achievement_image` フィールドを削除します。

### Documentation

#### [NEW] [README.md](file:///Users/nakamura/Downloads/codes/portfolio_ryo/README.md)

1.  **編集方法の記述**:
    - Hugo サーバーの起動方法 (`hugo server -D`)
    - Publication や Experience の編集方法、新しい項目の追加方法
    - 文法の注意点（Markdown、HTML）

## 修正内容の確認

### ブラウザでの確認
- `localhost:1313` にアクセスし、以下の点を確認します。
  - Achievement (Publication) の画像が中央に配置されていること。
  - Experience セクションから画像が消え、レイアウトが崩れていないこと。
  - 日本語・英語の両方のページで正しく反映されていること。

### ファイルの確認
- `README.md` が作成され、内容が正確であることを確認します。
