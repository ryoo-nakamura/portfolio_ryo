# 実装計画 - .gitignoreの作成

Gitの管理対象外とするファイルやディレクトリを指定する `.gitignore` を作成し、`git status` を整理します。

## 実施内容

### Root

#### [NEW] [.gitignore](file:///Users/nakamura/Downloads/codes/portfolio_ryo/.gitignore)
以下の項目を除外対象として追加します：
- `public/` (ビルド済みファイル)
- `resources/` (Hugoのキャッシュ)
- `_vendor/` (外部モジュール)
- `.hugo_build.lock` (ビルドロックファイル)
- `.DS_Store` (OS関連の不可視ファイル)

## 検証計画
- `git status` を実行し、`public/` や `resources/` が表示されなくなったことを確認します。
