<template>
  <div>
    <Navbar />
    <section class="home-hero">
      <h1>Strengthening communities in Goole and East Yorkshire</h1>
      <div class="home-hero-actions">
        <nuxt-link to="/about"
          ><b-button class="btn-primary">CTA</b-button></nuxt-link
        >
        <div class="home-hero-social-buttons">
          <img src="../assets/images/facebook (2).svg" alt="" />
          <img src="../assets/images/instagram.svg" alt="" />
          <img src="../assets/images/twitter (2).svg" alt="" />
        </div>
      </div>
    </section>
    <section class="section intro">
      <h2>Who we are</h2>
      <p>
        New Life Support is a project that aims to help young people. We want to
        give young people the best life possible. We do this through various
        activities, information, and support to help them make the choices that
        best fulfil their potential. <br />
        <br />
        Started in 2013, New Life Support has grown into a valuable resource for
        the young people of Goole to meet with professionals, experts, and
        mentors. It enables them to make the best use of their time and to gain
        key skills that help them achieve the best out of their lives.
      </p>
    </section>
    <section class="section section-cards">
      <h2>What we do</h2>
      <div class="cards-container">
        <b-card
          img-src="../assets/images/people-icon.svg"
          img-alt="people icon"
          img-top
          tag="article"
          style="max-width: 20rem"
          class="mb-2"
        >
          <p>Drop-in sessions</p>
          <nuxt-link to="/activities/youthwork"
            ><b-button class="btn-primary">Learn more</b-button></nuxt-link
          >
        </b-card>
        <b-card
          img-src="../assets/images/food2-icon.svg"
          img-alt="people icon"
          img-top
          tag="article"
          style="max-width: 20rem"
          class="mb-2"
        >
          <p>Lunchbox</p>
          <nuxt-link to="/activities/lunchboxgold"
            ><b-button class="btn-primary">Learn more</b-button></nuxt-link
          >
        </b-card>
        <b-card
          img-src="../assets/images/hands-icon.svg"
          img-alt="people icon"
          img-top
          tag="article"
          style="max-width: 20rem"
          class="mb-2"
        >
          <p>Youth Work</p>
          <nuxt-link to="/activities/youthwork"
            ><b-button class="btn-primary">Learn more</b-button></nuxt-link
          >
        </b-card>
      </div>
    </section>
    <section class="section section-banner">
      <h3 class="banner-quote">
        "We reach into the heart of this community. We are here building
        bridges."
      </h3>
      <p class="banner-attribution">
        - Jonathan Whitehouse <br />
        NLS Youth Worker
      </p>
    </section>
    <section class="section section-news-brief">
      <h2>News</h2>

      <NewsBrief />
    </section>
    <section class="section section-carousel">
      <h2>Get Involved</h2>
      <b-carousel
        id="carousel-1"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        background="#202020"
        img-width="1024"
        img-height="480"
        style="text-shadow: 1px 1px 2px #333"
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
      >
        <b-carousel-slide>
          <div class="carousel-content">
            <h3>Volunteering</h3>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque
              debitis ratione dolor, vel animi esse nulla, tempore adipisci,
              mollitia aut quam eum et consequatur numquam maxime similique
              aspernatur minima sunt?
            </p>
            <nuxt-link to="/about"
              ><b-button class="btn-primary">CTA</b-button></nuxt-link
            >
            <img class="carousel-image" src="../assets/images/3.jpg" alt="" />
          </div>
        </b-carousel-slide>
      </b-carousel>
    </section>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import NewsBrief from "~/components/NewsBrief.vue";

export default {
  name: "IndexPage",
  components: { Navbar, NewsBrief },
};
</script>

<style>
/*   */
.home-hero {
  background: linear-gradient(
      to right,
      rgba(50, 70, 80, 0.49),
      rgba(50, 70, 80, 0.49)
    ),
    url("../assets/images/home-hero3.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: 20% 5%;
  display: flex;
  flex-direction: column;
}
.btn-primary {
  width: 150px;
  border-radius: 20px;
  background-color: #ff5e98;
  border: none;
}
.btn-primary:hover {
  background-color: #172d4e;
}
.home-hero h1 {
  font-size: 3.5rem;

  color: #fff;
  font-family: "Roboto", sans-serif;

  font-weight: 800;
  margin-bottom: 2rem;
  text-shadow: 0px 0px 9px #000000;
}
.home-hero-actions {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: fit-content;
  gap: 1rem;
}
.home-hero-social-buttons {
  display: flex;
  gap: 1rem;
}
.section {
  padding: 5%;
}
.section h2 {
  color: #ff5e98;
  font-weight: bold;
  text-decoration: underline;
  text-align: center;
  margin-bottom: 2rem;
}
.cards-container {
  display: grid;
  grid-template-columns: auto;
  place-items: center;
  gap: 1rem;
}
.card {
  width: 100%;
  padding: 0.5rem;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: 0px 0px 5px 2px #b4b4b4;
}
.card-img-top {
  width: 80%;
}
.card-body {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0;
}
.card-body {
  font-size: 1.2rem;
}
.section-banner {
  padding: 20% 5%;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: linear-gradient(
      to right,
      rgba(50, 70, 80, 0.65),
      rgba(50, 70, 80, 0.65)
    ),
    url("../assets/images/banner.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  gap: 1.5rem;
}
.banner-quote {
  font-size: 2.5rem;
  font-weight: bold;
  color: #fff;
  text-shadow: 0px 0px 9px #000000;
}
.banner-attribution {
  font-size: 1rem;
  font-weight: bold;
  color: #ff5e98;
  text-shadow: 0px 0px 9px #000000;
}
.section-carousel {
  background-color: #202020;
  height: 800px;
}
.carousel {
  height: 100%;
}

.carousel-item {
  height: 700px;
}
.carousel-content {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.carousel-image {
  width: 100%;
}
@media all and (max-width: 480px) {
  .home-hero h1 {
    font-size: 2.5rem;
  }
}
@media all and (max-width: 576px) {
  .home-hero h1 {
    font-size: 2.5rem;
    width: 70%;
  }
  .home-hero {
    padding: 10% 5% 20% 5%;
  }
}
@media all and (min-width: 577px) and (max-width: 768px) {
  .home-hero {
    padding: 10% 5%;
  }
  .home-hero h1 {
    font-size: 4rem;
    width: 80%;
  }
  .section {
    padding: 10%;
    font-size: 1.2rem;
  }
  .section-cards {
    padding: 5%;
  }
  .cards-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
  .banner-quote {
    font-size: 3rem;
  }
  .banner-attribution {
    font-size: 1.5rem;
  }
  .section-news-brief {
    padding: 5%;
  }
}
@media all and (min-width: 769px) and (max-width: 992px) {
  .home-hero h1 {
    font-size: 4rem;
    width: 70%;
  }
  .home-hero {
    padding: 5% 5% 10% 5%;
  }
  .section {
    padding: 10%;
    font-size: 1.5rem;
  }
  .section-cards {
    font-size: 1.2rem;
  }
  .cards-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
  .banner-quote {
    font-size: 3rem;
  }
  .banner-attribution {
    font-size: 1.5rem;
  }
}
@media all and (min-width: 993px) and (max-width: 1200px) {
  .home-hero h1 {
    font-size: 5rem;
    width: 50%;
  }
  .home-hero {
    padding: 5% 10% 10% 10%;
  }
  .section {
    padding: 10% 15%;
    font-size: 1.5rem;
  }
  .btn-primary {
    width: 200px;
    padding: 0.5rem;
  }
  .cards-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
  .section-banner {
    padding: 10%;
  }
  .banner-quote {
    font-size: 4rem;
  }
  .banner-attribution {
    font-size: 2rem;
  }
  .section-news-brief {
    padding: 5%;
  }
}
@media all and (min-width: 1201px) and (max-width: 1400px) {
  .home-hero h1 {
    font-size: 5.5rem;
    width: 50%;
  }
  .home-hero {
    padding: 5% 10% 10% 10%;
  }
  .section {
    padding: 8% 20%;
    font-size: 1.5rem;
  }
  .btn-primary {
    width: 200px;
    padding: 0.5rem;
  }
  .cards-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
  .section-banner {
    padding: 10% 15%;
  }
  .banner-quote {
    font-size: 4rem;
  }
  .banner-attribution {
    font-size: 2rem;
    text-align: center;
  }
}
@media all and (min-width: 1401px) {
  .home-hero h1 {
    font-size: 5.5rem;
    width: 60%;
  }
  .home-hero {
    padding: 2% 15% 4% 15%;
  }
  .section {
    padding: 5% 20%;
    font-size: 1.5rem;
  }
  .btn-primary {
    width: 200px;
    padding: 0.5rem;
  }
  .cards-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
  .section-banner {
    padding: 5% 15%;
  }
  .banner-quote {
    font-size: 5rem;
  }
  .banner-attribution {
    font-size: 2rem;
    text-align: center;
  }
}
</style>
