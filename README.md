# runa.dev Blog Content

このリポジトリは [runa.dev](https://runa.dev) のブログコンテンツを管理するためのものです。

## フォルダ構造

```plaintext
.
├── posts/          # ブログ記事のMDXファイル
├── authors/        # 著者情報
└── images/         # 画像ファイル
    └── <slug>/     # 記事ごとの画像ディレクトリ
```

## メタデータ形式

### 記事のメタデータ (posts/*.mdx)

```yaml
---
title: 記事のタイトル
description: 記事の説明（SEO用）
date: YYYY-MM-DD
author: authors/の著者ID
tags: [tag1, tag2]
published: true|false
---
```

### 著者のメタデータ (authors/*.mdx)

```yaml
---
name: 著者名
avatar: アバター画像のURL
bio: 自己紹介
twitter: Twitterハンドル（オプション）
github: GitHubハンドル（オプション）
---
```

## 画像の使用方法

1. 画像は `images/<slug>/<image-name>.png` に配置します
2. MDXファイル内では `![alt text](slug/<image-name>.png)` で参照できます

例：

- 画像パス: `images/hello-world/screenshot.png`
- MDX内での参照: `![スクリーンショット](hello-world/screenshot.png)`

## 投稿の作成方法

1. `posts/` ディレクトリに `<slug>.mdx` ファイルを作成
2. 必要なメタデータを追加
3. 画像がある場合は `images/<slug>/` ディレクトリに配置
4. 本文を記述
5. プルリクエストを作成

### 注意事項/ガイドライン

- タイプミスや文法の修正は大歓迎です
- 技術的な内容の修正の場合は、できるだけ参考資料のリンクを含めていただけると嬉しいです
- 画像の追加・変更がある場合は、上記の画像配置ルールに従ってください
- プルリクエスト内で議論を行い、承認された後にマージされます
