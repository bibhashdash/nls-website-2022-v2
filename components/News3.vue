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
  name: "News3",

  async asyncData({ $content }) {
    const articles = await $content("articles").fetch();

    return { articles };
  },
};
</script>

<style>
ul,
li {
  list-style: none;
}
</style>
