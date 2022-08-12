<template>
  <div>
    <Navbar />
    <section class="home-hero">
      <h1>Strengthening communities in Goole and East Yorkshire</h1>
      <b-button class="btn-primary"
        ><nuxt-link to="/about">CTA</nuxt-link></b-button
      >
      <div class="home-hero-social-buttons">
        <img src="../assets/images/facebook (2).svg" alt="" />
        <img src="../assets/images/instagram.svg" alt="" />
        <img src="../assets/images/twitter (2).svg" alt="" />
      </div>
    </section>
    <!-- <NewsBrief /> -->
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
.home-hero {
  background: linear-gradient(
      to right,
      rgba(50, 70, 80, 0.74),
      rgba(50, 70, 80, 0.74)
    ),
    url(../assets/images/home-hero.jpg);
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
}
.home-hero h1 {
  font-size: 3.5rem;

  color: #fff;
  font-family: "Roboto", sans-serif;

  font-weight: 800;
  margin-bottom: 2rem;
}
.home-hero-social-buttons {
  margin-top: 1rem;
  margin-left: 2rem;
  display: flex;
  gap: 1rem;
}
@media all and (max-width: 480px) {
  .home-hero h1 {
    font-size: 2.5rem;
  }
}
@media all and (min-width: 576px) {
  .home-hero {
    padding: 10% 5%;
  }
  .home-hero h1 {
    font-size: 4rem;
  }
}
@media all and (min-width: 769px) {
  .home-hero h1 {
    font-size: 4rem;
  }
}
</style>
