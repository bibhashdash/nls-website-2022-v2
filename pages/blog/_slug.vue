<template>
  <div>
    <Navbar />
    <div class="article-wrapper">
      <article>
        <NuxtLink to="/blog"
          ><p style="color: #ff5e98; font-weight: bold">
            <span
              ><img
                src="../../assets/images/chevron_left_black_24dp.svg"
                alt=""
            /></span>
            Back to news
          </p></NuxtLink
        >
        <img
          class="blog-image"
          :src="require(`~/assets/images/blogImages/${article.img}`)"
          alt=""
        />
        <nuxt-content :document="article" />
        <NuxtLink to="/blog">
          <!-- <b-button class="btn-primary back-to-all-news"
            >Back to all news</b-button
          > -->
          <Button buttonContent="Back to all news" />
        </NuxtLink>
      </article>
    </div>
  </div>
</template>

<script>
import Button from "~/components/Interaction/Button.vue";
export default {
  name: "blog-slug",
  async asyncData({ $content, params }) {
    const article = await $content("articles", params.slug).fetch();
    return { article };
  },
  components: { Button },
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
  border-radius: 20px;
}
.article-wrapper a {
  align-self: flex-start;
}
</style>
