<script setup lang="ts">
import { Article } from "~~/src/types/api";

const { data } = await useAsyncData("hello", () =>
  $fetch("/api/article?id=m6p13qkyi")
);
const artilce = data as any as Article;
</script>
<template>
  <article class="mx-auto container px-2 md:px-4">
    <div class="znc" v-html="artilce.html"></div>
  </article>
</template>
