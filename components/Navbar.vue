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
        
       <b-nav-item-dropdown text="Get Involved" >
          <b-dropdown-item href="#"><nuxt-link to="/getinvolved/volunteer">Volunteer</nuxt-link></b-dropdown-item>
          <b-dropdown-item href="#"><nuxt-link to="/getinvolved/donate">Donate</nuxt-link></b-dropdown-item>
          <b-dropdown-item href="#"><nuxt-link to="/getinvolved/fundraise">Fundraise</nuxt-link></b-dropdown-item>
          
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
  position: fixed;
  width: 100%;
}
.navbar-collapse {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
}
.navbar-nav {
  align-items: center;
}
.bg-info {
  background-color: rgba(0, 0, 0, 0.619) !important;
}
a {
  margin-right: 1rem;
  margin-left: 1rem;
}
.logo {
  width: 60px;
}
.dropdown-menu {
  background-color: transparent;
}
</style>
