<template>
  <div>
    <Navbar />
    <section class="home-hero">
      <h1>Strengthening communities in Goole and East Yorkshire</h1>
      <b-button class="btn-primary"><nuxt-link to="/about">About</nuxt-link></b-button>
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
  background: linear-gradient(to right, rgba(50, 70, 80, 0.49), rgba(50, 70, 80, 0.49)), url(../assets/images/home-hero.jpg);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: 5% 10%;
}
.btn-primary {
  width: 150px;
  border-radius: 20px;
background-color: rgb(216, 5, 139);
}
.home-hero h1 {
  font-size: 5.5rem;
  width: 70%;
  color: #fff;

}
</style>
