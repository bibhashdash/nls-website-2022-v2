<template>
  <div>
    <Navbar />
    <h1>Welcome to the home section</h1>
    <NewsBrief />
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
