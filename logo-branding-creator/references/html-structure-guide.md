# Brand Guideline HTML 構造ガイド

このファイルは、Phase 4で生成するHTMLの設計仕様を記録したものです。
`brand-guideline-reference.html` が実際のサンプルです。

## セクション構成

| ID | eyebrow | タイトル | 主なUI要素 |
|----|---------|---------|-----------|
| #logo | 01 / LOGO SYSTEM | ロゴシステム | logo-grid（2col）、submark-row、logo-rule-grid（2col） |
| #color | 02 / COLOR | カラーパレット | color-grid（5col）、color-usage テーブル |
| #type | 03 / TYPOGRAPHY | タイポグラフィ階層 | type-scale（7行）、font-pair-grid（2col） |
| #brand | 04 / BRAND | ブランドパーソナリティ | personality-grid（5col）、tagline-grid（3col）、tone-grid（2col）、mission-box |
| #preview | 05 / PREVIEW | コンテキスト別プレビュー | preview-light、preview-dark |
| checklist | 06 / CHECKLIST | ブランドチェックリスト | checklist（10項目、クリック可能） |

## デザイントークン

- topbar: sticky, height 44px, backdrop-filter blur(12px)
- hero: background var(--dark), radial-gradient アクセント
- page: max-width 880px, padding 0 40px 120px
- section: padding-top 64px
- divider: height 0.5px, var(--border)
- border-radius: カード12px、小要素10px、バッジ99px
- border: 0.5px solid var(--border)

## カラーCSS変数の命名規則

```css
:root {
  --primary:      メインブランドカラー
  --primary-mid:  中間色（30%程度明るく）
  --primary-light: 淡色（60%程度明るく）
  --primary-pale: 極淡色（背景用、90%程度明るく）
  --dark:         ほぼ黒のテキスト色
  --dark-mid:     中間グレー（サブテキスト）
  --dark-light:   ライトグレー（キャプション）
  --off-white:    背景・サーフェス色
  --white:        純白
  --border:       rgba(dark, 0.12)
}
```

## ロゴSVGの実装パターン

### ワードマーク型
```svg
<svg viewBox="0 0 200 60" fill="none">
  <text x="0" y="44" font-family="DisplayFont" font-size="40" font-weight="500" fill="var(--primary)">BRAND</text>
</svg>
```

### アイコン＋ワードマーク型
```svg
<svg viewBox="0 0 240 60" fill="none">
  <!-- アイコン部分 -->
  <rect x="0" y="8" width="44" height="44" rx="10" fill="var(--primary)"/>
  <!-- ワードマーク -->
  <text x="56" y="42" font-family="DisplayFont" font-size="32" fill="var(--dark)">brand</text>
</svg>
```

### モノグラム型（サブマーク用）
```svg
<svg viewBox="0 0 56 56" fill="none">
  <rect width="56" height="56" rx="12" fill="var(--primary)"/>
  <text x="50%" y="50%" dominant-baseline="central" text-anchor="middle"
    font-family="DisplayFont" font-size="24" font-weight="600" fill="white">B</text>
</svg>
```

## チェックリストのインタラクティブ実装

```html
<div class="checklist-item" onclick="this.classList.toggle('checked')">
  <div class="checklist-box"></div>
  チェック項目のテキスト
</div>
```

```css
.checklist-item.checked .checklist-box {
  background: var(--primary);
  border-color: var(--primary);
}
.checklist-item.checked .checklist-box::after {
  content: '✓';
  color: white;
  font-size: 11px;
  display: flex;
  align-items: center;
  justify-content: center;
}
```
