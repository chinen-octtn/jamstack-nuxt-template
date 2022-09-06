# Jamstack Nuxt Template [WIP]

Jamstack で Web サイトを構築するテンプレートを作成します。

実務でも使える構成を目指します。テンプレートとしては汎用的で、構成はできるだけシンプルに、ライブラリ等も必要最小限にする方針です。

改善案、提案のための issue・プルリクエストは歓迎です。

## 前提

Web サイトと Web アプリではユーザーの利用目的が違うことから、機能や設計方針にも違いがあります。

ここでの「Web サイト」とは静的なウェブページの集まりであると定義します。記事のようなページを更新する部分は Headless CMS 等の API で事前取得して HTML に埋め込むようにします。

このような Web サイトでは状態（state）の変化がほとんどありません。Web アプリのようにユーザーの操作によって状態が変化し続ける構成は過剰になる可能性があるため、必要になったら追加するという方針でも良いでしょう。

## 主な構成

フレームワークは Nuxt 3 を採用します。

静的ジェネレーター、ルーティング等の Web サイト生成の最低限の要素が揃っていることが採用理由です。

Next.js も十分ですが参考になるコンテンツが多数公開されているため、当リポジトリでは Nuxt 3 をベースとします。

## Recommended Editor

- [Visual Studio Code](https://azure.microsoft.com/ja-jp/products/visual-studio-code/)（VS Code）

### Code Formatter

- Prettier ・・・ VS Code の[拡張機能](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)を使用
- EditorConfig・・・VS Code の[拡張機能](https://editorconfig.org/#overview)を使用

## 本リポジトリ制作時の開発環境（2022.08）

- Mac OS Monterey 12.5.1
- Node 16.15.1
- npm 8.11.0

## 設計に関するドキュメント

- [ディレクトリ構造について](docs/DIRECTLY.md)
- [コンポーネントについて](docs/COMPONENTS.md)

---

# Nuxt 3 Minimal Starter

Look at the [nuxt 3 documentation](https://v3.nuxtjs.org) to learn more.

## Setup

```bash
npm ci
```

## Development Server

Start the development server on http://localhost:3000

```bash
npm run dev
```

## Production

Build the application for production:

```bash
npm run generate
```

静的生成したファイルは、.output/public に出力されます。
