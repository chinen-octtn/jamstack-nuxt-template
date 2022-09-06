# コンポーネントについて

コンポーネントは大きく 2 種類に分けられます。

1. サイト内で汎用的に使える
2. 特定のページでしか使わない

この特徴によってディレクトリを分けて管理します。

## コンポーネントの import

Nuxt 3 では Auto Imports という機能があります。コンポーネント名から推測して自動インポートしてくれるため、Vue ファイルでは明示的にコンポーネントファイルの import が必要ありません。

Auto Imports を前提としたディレクトリ構成でコンポーネントを管理します。

## 1. サイト内で汎用的に使えるコンポーネント

例）

- 共通ヘッダーや共通フッター
- 見出し
- 汎用のボタン

サイト内のどのページでも使えるコンポーネントは、/src/components/ 直下に格納します。

```
/src/components/TheHeader.vue
/src/components/Heading.vue
/src/components/Button.vue
```

これらのコンポーネントは、テンプレート内でファイル名をタグのように使って呼び出すことができます。

```
<template>
  <TheHeader />
  <Heading />
  <Button />
</template>
```

## 2. 特定のページでしか使わないコンポーネント

例）

- 会社概要（/about/）のページ専用のコンポーネント
- サイトマップ（/sitemap/）のページ専用のコンポーネント

サイト内で特定のページ用のコンポーネントは /src/components/page/ページ名/ に格納します。

```
/src/components/page/about/KeyVisual.vue
/src/components/page/about/History.vue
```

これらのコンポーネントは、ディレクトリ名とファイル名をアッパーキャメルケースでつないだ名前で呼び出すことができます。

```
<template>
  <PageAboutKeyVisual />
  <PageAboutHistory />
</template>
```

## コンポーネント名

ヘッダーやフッターのようにページ内で 1 度しか使わないものはファイル名の先頭に `The` をつけます。

基本的に共通コンポーネントの命名は複数単語とするべきです。（同じファイル名だとエラーが起こるのを回避するため）
フォルダ構造が分かれている場合はその限りではありません。

例）

- Todo.vue // NG
- TodoItem.vue // OK

参照：[Vue.js スタイルガイド](https://jp.vuejs.org/v2/style-guide/index.html#%E5%8D%98%E4%B8%80%E3%82%A4%E3%83%B3%E3%82%B9%E3%82%BF%E3%83%B3%E3%82%B9%E3%81%AE%E3%82%B3%E3%83%B3%E3%83%9D%E3%83%BC%E3%83%8D%E3%83%B3%E3%83%88%E5%90%8D-%E5%BC%B7%E3%81%8F%E6%8E%A8%E5%A5%A8)
