<template>
  <div>
    <Navbar />
    <section class="home-hero">
      <h1>Strengthening communities in Goole and East Yorkshire</h1>
      <div class="home-hero-actions">
        <nuxt-link to="/about">
          <Button buttonContent="About Us" />
        </nuxt-link>
        <!-- <div class="home-hero-social-buttons">
          <img src="../assets/images/facebook (2).svg" alt="" />
          <img src="../assets/images/instagram.svg" alt="" />
          <img src="../assets/images/twitter (2).svg" alt="" />
        </div> -->
      </div>
    </section>
    <section class="section intro">
      <h2>Who we are</h2>
      <p>
        New Life Support aims to support young people and communities in Hull
        and East Yorkshire. We create opportunities, put on activities, provide
        information and support, to help people to fulfil their potential,
        improve their wellbeing and make good choices for the benefit of their
        lives and their communities. <br />
        <br />
        Started in 2013, New Life Support is the youth and community work
        charity that works with and alongside Revive Church UK, Hull, East
        Yorkshire and networks beyond the region.
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
          <nuxt-link to="/activities/youthwork">
            <Button buttonContent="Learn More" />
          </nuxt-link>
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
            ><Button buttonContent="Learn More"
          /></nuxt-link>
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
            ><Button buttonContent="Learn More"
          /></nuxt-link>
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
        :interval="10000"
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
            <div class="carousel-text-and-button">
              <h3>Volunteering</h3>
              <p>
                Volunteering is at the heart of the community work of New Life
                Support. We recognise and value all our volunteers and provide
                bespoke opportunities and support to help a volunteer get the
                best out of their time investment. We realise that time is
                precious and offer anyone interested a conversation over a
                cuppa, a chance to attend a taster/trial session, training, team
                building and a great sense of being part of the team.
              </p>
              <nuxt-link to="/getinvolved/volunteer"
                ><Button buttonContent="Learn More"
              /></nuxt-link>
            </div>

            <img class="carousel-image" src="../assets/images/3.jpg" alt="" />
          </div>
        </b-carousel-slide>

        <b-carousel-slide>
          <div class="carousel-content">
            <div class="carousel-text-and-button">
              <h3>Donate</h3>
              <p>
                The charity has been privileged to carry out grant funded youth
                and community work, with support from East Riding of Yorkshire
                Council, Hull City Council, Children in Need, Goole Fields
                Windfarm Community Fund and others. With that in mind, we are
                honoured when we receive financial gifts or gifts in kind from
                individuals, local businesses, or organisations. This giving not
                only helps us to continue the good work, but we also recognise
                the giving as a partnership.
              </p>
              <nuxt-link to="/getinvolved/donate"
                ><Button buttonContent="Learn More"
              /></nuxt-link>
            </div>

            <img class="carousel-image" src="../assets/images/2.jpg" alt="" />
          </div>
        </b-carousel-slide>
        <b-carousel-slide>
          <div class="carousel-content">
            <div class="carousel-text-and-button">
              <h3>Fundraise</h3>
              <p>
                Whether you love baking, walking, football or bingo, we have
                plenty of ideas of how you can fundraise and help transform the
                lives of young people and local communities. And you don't even
                have to sit in a tub of baked beans to do it (unless you really
                want to)! From an Auction to a Zumba party, check out our
                fundraising page for inspiration and details on how to get
                involved.
              </p>
              <nuxt-link to="/getinvolved/fundraise"
                ><Button buttonContent="Learn More"
              /></nuxt-link>
            </div>

            <img
              class="carousel-image"
              src="../assets/images/home-fundraise.jpg"
              alt=""
            />
          </div>
        </b-carousel-slide>
      </b-carousel>
    </section>
    <section class="section section-banner contact-banner">
      <h3 class="banner-quote">
        For any questions or to learn more about what we do, drop us a message!
      </h3>
      <nuxt-link to="/contact"><Button buttonContent="Contact Us" /></nuxt-link>
    </section>
    <Footer />
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import NewsBrief from "~/components/NewsBrief.vue";
import Footer from "~/components/Footer.vue";
import Button from "~/components/Interaction/Button.vue";

export default {
  name: "IndexPage",
  components: { Navbar, NewsBrief, Footer, Button, Button },
};
</script>

<style>
/*   */
.home-hero {
  background: linear-gradient(
      to right,
      rgba(0, 0, 0, 0.29),
      rgba(0, 0, 0, 0.29)
    ),
    url("../assets/images/home-hero5.jpg");

  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: 20% 5%;
  display: flex;
  flex-direction: column;
}

.home-hero h1 {
  font-size: 3.5rem;

  color: #fff;

  font-weight: 800;
  margin-bottom: 2rem;
  text-shadow: 0px 0px 9px #000000;
  /* align-self: flex-end; */
}
.home-hero-actions {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: fit-content;
  gap: 1rem;
  /* align-self: flex-end; */
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
.intro p {
  color: #000000;
}
.cards-container {
  display: grid;
  grid-template-columns: auto;
  place-items: center;
  gap: 1rem;
}
.card {
  width: 100%;
  padding: 1rem 0.5rem;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: 0px 0px 5px 2px #dddddd7b;
  border: none;
}
.card p {
  color: #000000;
}
.card-img-top {
  width: 40%;
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
  /* height: 800px; */
}

.carousel-item {
  height: 700px;
}
.carousel-content {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.carousel-content p {
  font-size: 1rem;
}
.carousel-caption {
  top: 0 !important;
}
.carousel-text-and-button {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.carousel-image {
  width: 100%;
  border-radius: 20px;
}
.contact-banner {
  background: #fff;
}
.contact-banner h3 {
  color: #000000;
  text-shadow: none;
}
@media all and (max-width: 480px) {
  .home-hero h1 {
    font-size: 2.5rem;
  }
}
@media all and (max-width: 576px) {
  .home-hero h1 {
    font-size: 2.5rem;
    /* width: 70%; */
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
    /* width: 80%; */
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
    width: 90%;
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
  .carousel-item {
    height: 900px;
  }
  .contact-banner h3 {
    font-size: 2rem;
  }
}
@media all and (min-width: 993px) and (max-width: 1200px) {
  .home-hero h1 {
    font-size: 5rem;
    /* width: 50%; */
  }
  .home-hero {
    padding: 5% 10% 10% 10%;
  }
  .section {
    padding: 10% 15%;
    font-size: 1.5rem;
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
  .carousel-item {
    height: 900px;
  }
  .contact-banner h3 {
    font-size: 2rem;
    width: 85%;
  }
}
@media all and (min-width: 1201px) and (max-width: 1400px) {
  .home-hero h1 {
    font-size: 5.5rem;
    /* width: 50%; */
  }
  .home-hero {
    padding: 5% 10% 10% 10%;
  }
  .section {
    padding: 8% 20%;
    font-size: 1.5rem;
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
  .carousel-item {
    height: 900px;
  }
  .contact-banner h3 {
    font-size: 2rem;
    width: 80%;
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
  .carousel-item {
    height: 900px;
  }
  .contact-banner h3 {
    font-size: 2rem;
    width: 70%;
  }
}
</style>
