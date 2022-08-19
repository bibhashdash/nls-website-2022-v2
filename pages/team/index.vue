<template>
  <div>
    <Navbar />
    <SecondaryHero mainTitle="Our Team" />
    <Footer />
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
import Footer from "~/components/Footer.vue";
import SecondaryHero from "~/components/SecondaryHero.vue";
export default {
  components: { Navbar, Footer, SecondaryHero },
};
</script>

<style></style>
