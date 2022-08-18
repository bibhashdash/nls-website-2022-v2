<template>
  <section class="secondary-hero">
    <h1>{{ mainTitle }}</h1>
  </section>
</template>

<script>
export default {
  name: "SecondaryHero",
  props: ["mainTitle"],
};
</script>

<style>
.secondary-hero {
  background: linear-gradient(
      to right,
      rgba(50, 70, 80, 0.55),
      rgba(50, 70, 80, 0.55)
    ),
    url("../assets/images/secondary-hero.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: 15% 5%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  color: #fff;

  font-weight: 800;

  text-shadow: 0px 0px 9px #000000;
}
.secondary-hero h1 {
  font-size: 3rem;
}
@media all and (min-width: 481px) and (max-width: 576px) {
  .secondary-hero {
    padding: 10% 5%;
  }
  .secondary-hero h1 {
    font-size: 4rem;
  }
}
@media all and (min-width: 577px) and (max-width: 768px) {
  .secondary-hero {
    padding: 8% 5%;
  }
  .secondary-hero h1 {
    font-size: 4rem;
  }
}
@media all and (min-width: 769px) and (max-width: 992px) {
  .secondary-hero {
    padding: 8% 5%;
  }
  .secondary-hero h1 {
    font-size: 4rem;
  }
}
@media all and (min-width: 992px) {
  .secondary-hero {
    padding: 8% 5%;
    background-position: center;
  }
  .secondary-hero h1 {
    font-size: 5rem;
  }
}
</style>
