<script setup lang="ts">
// ベースとなるmeta情報
useHead({
  meta: [
    { name: "format-detection", content: "telephone=no" },
    { property: "og:type", content: "article" },
    { property: "og:site_name", content: "サイト名" },
    {
      property: "og:image",
      content: "https://example.com/ogp.png",
    },
    {
      name: "twitter:card",
      content: "summary_large_image",
    },
  ],
  link: [
    {
      rel: "shorcut icon",
      href: "/favicon.ico",
    },
    {
      rel: "apple-touch-icon",
      href: "/apple-touch-icon.png",
    },
  ],
});
</script>

<template>
  <div>
    <TheHeader />
    <main>
      <NuxtPage />
    </main>
    <TheFooter />
  </div>
</template>
