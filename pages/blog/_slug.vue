<template>
  <div>
    <Navbar />
    <article>
      <img
        class="blog-image"
        :src="require(`~/assets/images/${article.img}`)"
        alt=""
      />
      <nuxt-content :document="article" />
    </article>
  </div>
</template>

<script>
export default {
  name: "blog-slug",
  async asyncData({ $content, params }) {
    const article = await $content("articles", params.slug).fetch();

    return { article };
  },
  //   data() {
  //     return {
  //       imgSrc: "require(`../../static/images/${article.img}.jpg`)",
  //     };
  //   },
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
</style>
