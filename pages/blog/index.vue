<template>
  <div>
    <Navbar />
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
import Navbar from "~/components/Navbar.vue";

export default {
  components: { Navbar },
  async asyncData({ $content }) {
    const articles = await $content("articles").fetch();

    return { articles };
  },
};
</script>

<style></style>
