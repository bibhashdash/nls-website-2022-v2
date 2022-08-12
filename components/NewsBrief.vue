<template>
  <div>
    <h1>Hello world</h1>
    <p>
      {{ articles }}
    </p>
    <!-- <ul>
      <li v-for="article of articles" :key="article.slug">
        <NuxtLink
          :to="{
            name: 'blog-slug',
            params: {
              slug: article.slug,
            },
          }"
          ><p>{{ article.title }}</p>
        </NuxtLink>
      </li>
    </ul> -->
  </div>
</template>

<script>
export default {
  data() {
    return { articles: [] };
  },

  async fetch({ $content }) {
    this.articles = await $content("articles").fetch();
  },
};
</script>

<style>
ul,
li {
  list-style: none;
}
</style>
