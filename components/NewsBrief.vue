<template>
  <div>
    <ul>
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
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return { articles: [] };
  },

  async asyncData({ $content }) {
    this.articles = await $content("articles", { deep: true }).fetch();
    console.log(articles);
  },
};
</script>

<style>
ul,
li {
  list-style: none;
}
</style>
