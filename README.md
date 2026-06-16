# logo-branding-creator

ブランドの**ロゴとブランドアイデンティティをゼロから段階的に作り上げる** [Claude](https://claude.ai) 用スキルです。起業家・個人事業主・ブランディング初心者でも、専門知識なしで使えるよう、1問ずつのヒアリングから丁寧に案内します。

最後にはブランド情報を1ファイルにまとめた **ブランドガイドラインHTML** を自動生成します。

> 💡 Claude の「スキル（Skill / SKILL.md）」機能で動作します。**Claude Code** でも **Claude チャット版** でも、どちらでも使えます。

---

## ✨ 特長

- **1問ずつのヒアリング**で、専門知識ゼロでも答えられる
- ブランド戦略 → ロゴコンセプト → 批評 → ガイドライン → 最終決定まで**一貫したワークフロー**
- 各ステップで**確認・承認**を取りながら進むので置いていかれない
- AIロゴ生成ツール（Midjourney / Adobe Firefly / DALL-E 等）に貼り付けられる**日本語プロンプト**も生成
- 完成品として**ブランドガイドラインHTML**を出力（そのままブラウザで開ける）

## 🔄 ワークフロー

```
Phase 0: ヒアリング（共通情報を1問ずつ収集）
    ↓
Phase 1: ブランドアイデンティティ確立
    ↓
Phase 2: ロゴコンセプト複数案生成（AIプロンプト付き）
    ↓
Phase 3: ロゴ批評・絞り込み
    ↓
Phase 4: ブランドガイドラインHTML生成
    ↓
Phase 5: 最終ロゴ決定
```

## 📦 インストール

このリポジトリの `logo-branding-creator/` フォルダが、実際のスキル本体です。

### Claude Code で使う場合

`logo-branding-creator/` フォルダを、スキル置き場にコピーします。

- **全プロジェクトで使う場合**: `~/.claude/skills/` にコピー
- **特定のプロジェクトでだけ使う場合**: そのプロジェクトの `.claude/skills/` にコピー

```bash
# 例：このリポジトリをクローンして、全体共通のスキルとして配置
git clone https://github.com/<your-account>/logo-branding-creator.git
cp -r logo-branding-creator/logo-branding-creator ~/.claude/skills/
```

配置後に Claude Code を起動し直せば、自動で認識されます。

### Claude チャット版で使う場合

`logo-branding-creator/` フォルダを ZIP にまとめ、Claude の設定画面（Capabilities → Skills）からアップロードしてください。

## 🚀 使い方

インストール後、Claude に次のように話しかけるだけで起動します。

- 「ロゴを作りたい」
- 「ブランディングしたい」
- 「ブランドガイドラインを作って」
- 「logo」「branding」

あとは Claude の質問に1問ずつ答えていけば、ロゴの方向性とブランドガイドラインが出来上がります。

## 🙏 クレジット / Acknowledgements

このスキルのワークフローは、**Hamidullah Khan, PhD ([@IamKhanPhD](https://x.com/iamkhanphd))** さんが X に投稿したスレッド *"GOODBYE LOGO DESIGNERS IN 2026"* の10個のプロンプトに**インスパイアされて**設計しました。元のアイデアに感謝します。

- 元スレッド: https://x.com/iamkhanphd/status/2066279584710959384

> 本リポジトリには元スレッドの本文は含めていません。元のプロンプト全文は上記リンク先の投稿をご覧ください。SKILL.md の内容は、元のアイデアをもとに日本語の段階的ワークフローとして独自に再構成・拡張したものです。

## 📄 ライセンス

[MIT License](./LICENSE) のもとで公開しています。自由に利用・改変・再配布できます。
