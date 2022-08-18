<template>
  <div>
    <Navbar />
    <div class="article-wrapper">
      <article>
        <img
          class="blog-image"
          :src="require(`~/assets/images/${article.img}`)"
          alt=""
        />
        <nuxt-content :document="article" />
        <NuxtLink to="/blog"
          ><b-button class="btn-primary">Back to all news</b-button></NuxtLink
        >
      </article>
    </div>
  </div>
</template>

<script>
export default {
  name: "blog-slug",
  async asyncData({ $content, params }) {
    const article = await $content("articles", params.slug).fetch();

    return { article };
  },
};
</script>

<style scoped>
.article-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 5% 10%;
}
article {
  width: 100%;
  max-width: 1000px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.blog-image {
  width: 100%;
  max-width: 800px;
}
.article-wrapper a {
  align-self: flex-start;
}
</style>
