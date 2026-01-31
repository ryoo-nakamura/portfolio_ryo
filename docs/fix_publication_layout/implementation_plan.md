# 学会画像の追加とレイアウト統一の実装計画 (追加依頼反映版)

作成された学会画像を各論文項目に紐付け、すべての画像あり項目を 50:50 分割（高さ 200px）のレイアウトに統一します。

## 変更内容

### [Component] Content (Publications)

#### [MODIFY] [publications.md (ja)](file:///Users/nakamura/Downloads/codes/portfolio_ryo/content/ja/home/publications.md)
#### [MODIFY] [publications.md (en)](file:///Users/nakamura/Downloads/codes/portfolio_ryo/content/en/home/publications.md)

1.  **画像の追加と構造変更**:
    - 以下の項目を「画像なし（col-12）」または「古いレイアウト」から「50:50 分割（col-md-6 x 2）」の構造に変更し、画像パスを設定します。
    - **Simple variational inference...**: `information_geometry.png`
    - **On the Relationship Between Double Descent...**: `double_descent.png`
    - **Primitive Geometry Segment Pre-training for 3D Medical...**: `bmvc.png`
    - **Traffic Incident Database...**: `IROS.png`
    - **Rough Target Region Extraction...**: `iw-fcv.jpeg`
    

2.  **レイアウトの統一**:
    - すべての画像あり項目（既存・新規ともに）を `col-md-6` / 高高 `200px` の設定で統一します。

## 検証計画

### 手動確認
- ブラウザ (localhost:1313) で、指定した画像が正しく表示され、レイアウトが崩れていないことを確認します。
- 日本語版と英語版の両方で齟齬がないか確認します。
