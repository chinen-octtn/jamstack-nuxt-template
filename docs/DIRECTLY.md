# ディレクトリ構造について

## Nuxt ディレクトリ

Nuxt の初期値では、コンテンツを管理するディレクトリはリポジトリのルート直下が基準となっています。

ルート直下では config ファイルやライブラリの設定ファイルと混ざってしまい見通しが良くないため、Nuxt が扱うファイルは、`src/` 配下にまとめることとします。

※[nuxt.config.ts](./nuxt.config.ts)で基準となるディレクトリを指定

```
export default defineNuxtConfig({
  srcDir: "src/",
});
```

## src/components

コンポーネントを格納します。

参照：[Components Directory](https://v3.nuxtjs.org/guide/directory-structure/components)

## src/layouts

ページレイアウトのテンプレートとなるファイルを格納します。src/layouts/default.vue がデフォルトのテンプレートとしてすべてのページに適用されます。

例外のレイアウトとなるページが存在する場合は、src/layouts 配下に別のテンプレートとなる Vue ファイルを作成します。

参照：[Layouts Directory](https://v3.nuxtjs.org/guide/directory-structure/layouts)

## src/public

加工する必要のない静的ファイルを格納します。ファイル名がそのまま公開環境に設置されます。

例）

- favicon.ico
- manifest.json

ページ内で使う画像も何らかの処理が必要ない（画像をそのまま使う）場合は、public ディレクトリに格納することを推奨します。

参照：[Public Directory](https://v3.nuxtjs.org/guide/directory-structure/public)
