<template>
  <div>
    <Navbar />
    <SecondaryHero mainTitle="Donate" />
    <TempComponent />
    <Footer />
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
import Footer from "~/components/Footer.vue";
import SecondaryHero from "~/components/SecondaryHero.vue";
import TempComponent from "~/components/TempComponent.vue";
export default {
  components: { Navbar, Footer, SecondaryHero, TempComponent },
};
</script>

<style></style>
