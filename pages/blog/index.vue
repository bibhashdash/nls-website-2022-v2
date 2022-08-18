<template>
  <div>
    <Navbar />
    <h1>News Life Support</h1>
    <ul class="news-grid">
      <li v-for="article of articles" :key="article.slug">
        <NuxtLink
          :to="{
            name: 'blog-slug',
            params: {
              slug: article.slug,
            },
          }"
        >
          <img
            class="blog-image"
            :src="require(`~/assets/images/${article.img}`)"
            alt=""
          />
          <p>{{ article.title }}</p>
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

<style scoped>
ul,
li {
  list-style: none;
}
.news-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
.blog-image {
  width: 200px;
}
</style>
