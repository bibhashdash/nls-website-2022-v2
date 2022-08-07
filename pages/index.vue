<template>
  <div>
    <Navbar />
    <h1>Welcome to the home section</h1>
    <News3 />
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import News3 from "~/components/News3.vue";

export default {
  name: "IndexPage",
  components: { Navbar, News3 },
};
</script>
