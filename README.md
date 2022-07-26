# Jamstack Nuxt Template [WIP]

Jamstack で Web サイトを構築するテンプレートを作成します。

実務でも使える構成を目指します。テンプレートとしては汎用的で、構成はできるだけシンプルに、ライブラリ等も必要最小限にする方針です。

改善案、提案のための issue・プルリクエストは歓迎です。

## 前提

Web サイトと Web アプリではユーザーの利用目的が違うことから、機能や設計方針にも違いがあります。

ここでは「Web サイト」とは静的なウェブページの集まりであると定義します。記事コンテンツのようなページを更新する部分は Headless CMS 等の API で事前取得して HTML に埋め込むようにします。

このような Web サイトでは状態（state）の変化がほとんどありません。Web アプリのようにユーザーの操作によって状態が変化する構成は過剰になる可能性があります。

## 主な構成

フレームワークは Nuxt 3 を採用します。

静的ジェネレーター、ルーティング等の Web サイト生成の最低限の要素が揃っていることが採用理由です。

Next.js も十分ですがそちらは参考になるものが別途あるため、当リポジトリでは Nuxt3 をベースとします。

## Recommended Editor

- [Visual Studio Code](https://azure.microsoft.com/ja-jp/products/visual-studio-code/)（VS Code）

### Code Formatter

- Prettier ・・・ VS Code の[拡張機能](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)を使用
- EditorConfig・・・VS Code の[拡張機能](https://editorconfig.org/#overview)を使用

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
