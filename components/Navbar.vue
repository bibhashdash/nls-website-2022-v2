<template>
  <div>
    <b-navbar toggleable="lg" type="light" variant="light">
      <b-navbar-nav>
        <nuxt-link to="/">Home</nuxt-link>

        <!-- Navbar dropdowns -->
        <nuxt-link to="/news">News</nuxt-link>
        <nuxt-link to="/blog">Blog</nuxt-link>
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
a {
  margin-right: 1rem;
  margin-left: 1rem;
}
</style>
