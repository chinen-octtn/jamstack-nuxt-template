# Jamstack Nuxt Template [WIP]

JamstackでWebサイトを構築するテンプレートを作成します。

実務でも使える構成を目指します。テンプレートとしては汎用的で、構成はできるだけシンプルに、ライブラリ等も必要最小限にする方針です。

改善案、提案のためのissue・プルリクエストは歓迎です。

## 前提
WebサイトとWebアプリではユーザーの利用目的が違うことから、機能や設計方針にも違いがあります。

ここでは「Webサイト」とは静的なウェブページの集まりであると定義します。記事コンテンツのようなページを更新する部分はHeadless CMS等のAPIで事前取得してHTMLに埋め込むようにします。

このようなWebサイトでは状態（state）の変化がほとんどありません。Webアプリのようにユーザーの操作によって状態が変化する構成は過剰になる可能性があります。

## 主な構成
フレームワークはNuxt 3を採用します。

静的ジェネレーター、ルーティング等のWebサイト生成の最低限の要素が揃っていることが採用理由です。

Next.jsも十分ですがそちらは参考になるものが別途あるため、当リポジトリではNuxt3をベースとします。



# Nuxt 3 Minimal Starter

Look at the [nuxt 3 documentation](https://v3.nuxtjs.org) to learn more.

## Setup

Make sure to install the dependencies:

```bash
# yarn
yarn install

# npm
npm install

# pnpm
pnpm install --shamefully-hoist
```

## Development Server

Start the development server on http://localhost:3000

```bash
npm run dev
```

## Production

Build the application for production:

```bash
npm run build
```

Locally preview production build:

```bash
npm run preview
```

Checkout the [deployment documentation](https://v3.nuxtjs.org/guide/deploy/presets) for more information.
