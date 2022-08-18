<template>
  <div>
    <Navbar />
    <SecondaryHero mainTitle="News" />
    <div class="section section-news-grid">
      <h2>All the latest</h2>
      <ul class="news-grid">
        <li v-for="article of articles" :key="article.slug">
          <img
            class="blog-image"
            :src="require(`~/assets/images/${article.img}`)"
            alt=""
          />

          <p class="article-title">{{ article.title }}</p>
          <p class="article-date">{{ article.date }}</p>
          <p class="article-summary">{{ article.summary }}</p>

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
                ><img
                  src="../../assets/images/chevron_right_black_24dp.svg"
                  alt=""
              /></span></p
          ></NuxtLink>
        </li>
      </ul>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
import SecondaryHero from "~/components/SecondaryHero.vue";
import Footer from "~/components/Footer.vue";

export default {
  components: { Navbar, SecondaryHero, Footer },
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
.section-news-grid {
  padding: 5%;
}
.news-grid {
  display: grid;
  grid-template-columns: auto;
}
.blog-image {
  width: 100%;
}
.article-title {
  color: black;
  font-weight: bold;
  font-size: 1.5rem;
}
.article-summary {
  color: black;
  font-size: 1rem;
}
.article-date {
  color: rgb(102, 102, 102);
  font-size: 0.8rem;
}
@media all and (min-width: 577px) {
  .news-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }
}
@media all and (min-width: 993px) {
  .news-grid {
    gap: 2rem;
    padding: 5% 10%;
  }
}
</style>
