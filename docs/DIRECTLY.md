# ディレクトリ構造について

## Nuxt ディレクトリ

Nuxt の初期値では、コンテンツを管理するディレクトリはリポジトリのルート直下が基準となっています。

ルート直下ではライブラリ関連の設定ファイルや config ファイルが多くなり見通しが悪くなりやすいため、Nuxt が扱うファイルは、`src/` 配下にまとめることとします。

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

別のレイアウトを追加する場合は、src/layouts 配下に別のテンプレートとなる Vue ファイルを作成します。

参照：[Layouts Directory](https://v3.nuxtjs.org/guide/directory-structure/layouts)

## src/pages

Nuxt は、[Vue Router](https://router.vuejs.org/)を利用してファイルベースのルーティングを提供しています。

pages ディレクトリの直下がドキュメントルートなるように、ディレクトリ・ファイルを配置します。

## src/public

とくに加工しない静的ファイルを格納します。`src/public` 配下のディレクトリ・ファイル名がそのまま公開環境に設置されます。

例）

- favicon.ico
- manifest.json

ページ内で使う画像も加工せずにそのまま使う場合は、public ディレクトリに格納します。

参照：[Public Directory](https://v3.nuxtjs.org/guide/directory-structure/public)
