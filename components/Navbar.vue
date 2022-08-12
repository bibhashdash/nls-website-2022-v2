<template>
 
  <div class="nav-wrapper">
  <b-navbar toggleable="lg" type="dark" variant="info">
    <b-navbar-brand href="https://nls-prototype.netlify.app/">
      <img class="logo" src="../assets/images/NLS_round_logo_gold.png" alt="">
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <nuxt-link to="/">Home</nuxt-link>
        <nuxt-link to="/blog">Blog</nuxt-link>
        <nuxt-link to="/about">About</nuxt-link>
        <nuxt-link to="/contact">Contact</nuxt-link>
        
       <b-nav-item-dropdown text="Lang" >
          <b-dropdown-item href="#">EN</b-dropdown-item>
          <b-dropdown-item href="#">ES</b-dropdown-item>
          <b-dropdown-item href="#">RU</b-dropdown-item>
          <b-dropdown-item href="#">FA</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>

      
    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
.nav-wrapper {
  background-color: transparent !important;
}
a {
  margin-right: 1rem;
  margin-left: 1rem;
}
.logo {
  width: 60px;
}
</style>
