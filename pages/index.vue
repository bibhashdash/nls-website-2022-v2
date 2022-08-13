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
    <section class="intro">
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
    <section class="_cards">
      <div>
        <div class="_card"></div>
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
/*   */
.home-hero {
  background: linear-gradient(
      to right,
      rgba(50, 70, 80, 0.49),
      rgba(50, 70, 80, 0.49)
    ),
    url("../assets/images/home-hero2.jpg");
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
  text-shadow: 0px 0px 9px #000000;
}
.home-hero-social-buttons {
  margin-top: 1rem;
  margin-left: 2rem;
  display: flex;
  gap: 1rem;
}
.intro {
  padding: 5%;
}
.intro h2 {
  color: #ff5e98;
  font-weight: bold;
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
    width: 70%;
  }
  .intro {
    padding: 10%;
    font-size: 1.2rem;
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
  .intro {
    padding: 10%;
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
  .intro {
    padding: 10% 15%;
    font-size: 1.5rem;
  }
}
@media all and (min-width: 1201px) and (max-width: 1400px) {
  .home-hero h1 {
    font-size: 6rem;
    width: 50%;
  }
  .home-hero {
    padding: 5% 10% 10% 10%;
  }
  .intro {
    padding: 10% 20%;
    font-size: 1.5rem;
  }
}
@media all and (min-width: 1401px) {
  .home-hero h1 {
    font-size: 6rem;
    width: 50%;
  }
  .home-hero {
    padding: 2% 15% 2% 15%;
  }
  .intro {
    padding: 5% 20%;
    font-size: 1.5rem;
  }
}
</style>
