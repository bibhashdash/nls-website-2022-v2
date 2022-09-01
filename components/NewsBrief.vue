<template>
  <div class="news-brief-component">
    <ul class="news-brief-cards-container">
      <li
        class="news-brief-card"
        v-for="article of articles"
        :key="article.slug"
      >
        <img
          class="blog-image"
          :src="require(`~/assets/images/blogImages/${article.img}`)"
          alt=""
        />
        <p class="news-brief-title">{{ article.title }}</p>
        <p class="news-brief-summary">{{ article.summary.slice(0, 100) }}...</p>
        <NuxtLink
          :to="{
            name: 'blog-slug',
            params: {
              slug: article.slug,
            },
          }"
          ><p class="read-more">
            Read More
            <span
              ><img src="../assets/images/chevron_right_black_24dp.svg" alt=""
            /></span></p
        ></NuxtLink>
      </li>
    </ul>
    <nuxt-link to="/blog">
      <Button buttonContent="See all news" />
    </nuxt-link>
  </div>
</template>

<script>
import Button from "./Interaction/Button.vue";
export default {
  data() {
    return { articles: [] };
  },
  async fetch() {
    this.articles = await this.$content("articles")
      .limit(4)
      .sortBy("index", "desc")
      .fetch();
  },
  components: { Button },
};
</script>

<style>
.news-brief-component {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;
}
ul,
li {
  list-style: none;
  padding: 0;
  margin: 0;
}
.news-brief-cards-container {
  display: grid;
  grid-template-columns: auto;
  place-items: center;
  width: 100%;
  gap: 1rem;
}
.news-brief-card {
  width: 100%;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  display: flex;
  flex-direction: column;

  box-shadow: 0px 0px 5px 2px #b4b4b4;
}
.blog-image {
  width: 100%;
  border-radius: 20px;
}
.news-brief-title {
  color: black;
  font-size: 1.5rem;
  font-weight: bold;
  align-self: flex-start;
}
.news-brief-summary {
  color: black;
  align-self: flex-start;
}
.read-more {
  color: #ff5e98;
  font-weight: bold;
}
.news-brief-card a {
  align-self: flex-start;
  font-size: 1rem;
}
@media all and (min-width: 577px) {
  .news-brief-cards-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    place-items: center;
    width: 100%;
    gap: 1rem;
  }
  .news-brief-card {
    width: 100%;
    padding: 0.5rem;
    border-radius: 20px;
    display: flex;
    flex-direction: column;

    box-shadow: 0px 0px 5px 2px #b4b4b4;
  }
  .news-brief-summary {
    font-size: 1rem;
  }
}
@media all and (min-width: 993px) {
  .news-brief-cards-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    place-items: center;
    width: 100%;
    gap: 1rem;
  }
  .news-brief-card {
    padding: 1rem;
  }
}
</style>
