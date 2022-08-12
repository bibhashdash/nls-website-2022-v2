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
          ><img
        class="blog-image"
        :src="require(`~/assets/images/${article.img}`)"
        alt=""
      /><p>{{ article.title }}</p>
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

  async fetch() {
    this.articles = await this.$content("articles").limit(3).fetch();
  },
};
</script>

<style>
ul,
li {
  list-style: none;
}
.blog-image {
  width: 200px;
}
</style>
