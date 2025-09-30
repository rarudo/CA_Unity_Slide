# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

このリポジトリは、Marpフレームワークを使用したプレゼンテーションスライドのプロジェクトです。

## プロジェクト構造

```
0711-opera-ai-slide/
├── slide.md        # メインのプレゼンテーションMarkdownファイル
├── slide.html      # 生成されたHTMLファイル
├── css/
│   ├── style.css   # カスタムMarpテーマ
│   └── *.png       # ロゴ画像
├── resources/      # プレゼンテーションで使用する画像・動画ファイル
└── requirements/   # 過去のスライド更新時の要件記録
    ├── update1.md  # 過去の更新要件（参考情報）
    └── update2.md  # 過去の更新要件（参考情報）
```

**注意**: `requirements/`ディレクトリ内のファイルは過去のスライド更新時の要件を記録したものです。これらは文脈理解の参考にはなりますが、最新のスライド内容とは異なる場合があります。

## Marpのソースコード参照

Marpの使い方や機能について迷った際は、以下のソースコードディレクトリを参照してください：

- **marp-cli** (`/Users/s02649/Documents/Workspace/marp/marp-cli/`): CLIツールの実装
  - `src/cli.ts`: コマンドライン引数の処理
  - `src/converter.ts`: Markdown→HTML/PDF/PPTX変換の実装
  - `src/engine.ts`: Marpエンジンの設定

- **marp-core** (`/Users/s02649/Documents/Workspace/marp/marp-core/`): Marpのコア機能
  - `src/marp.ts`: Marpクラスの実装
  - `themes/`: 組み込みテーマ（default, gaia, uncover）
  - `src/math/`: 数式レンダリング（KaTeX/MathJax）
  - `src/emoji/`: 絵文字サポート

- **marpit** (`/Users/s02649/Documents/Workspace/marp/marpit/`): Marpitフレームワーク
  - `src/markdown/`: Markdownパーサーの拡張
  - `src/theme.js`: テーマシステムの実装

## カスタムテーマについて

`css/style.css`はカスタムテーマファイルです。以下のクラスが定義されています：

- `.title`: タイトルスライド
- `.section`: セクション見出しスライド
- `.content`: コンテンツスライド
- `.prompt-example`: プロンプト例表示用のスタイル
- `.highlight-box`: 強調ボックス

## スライド作成ルール

スライドを編集する際は、以下のドキュメントに記載されている文章スタイル・口調・情報量のガイドラインに従ってください：

📝 [スライド作成ルール](.claude/docs/slide-rules.md)

## slide.mdを更新した場合
slide.mdを更新した場合以下の手順を実行してgitコミットを行う

```bash
git add -A slide.md
git commit -m "適切なコミットメッセージ"
```
