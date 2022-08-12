<template>
  <b-navbar toggleable="lg" variant="info">
    <b-navbar-brand href="https://nls-prototype.netlify.app/">
      <img class="logo" src="../assets/images/NLS_round_logo_gold.png" alt="" />
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"
      ><span class="menu-bar">Menu</span></b-navbar-toggle
    >

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <nuxt-link to="/">Home</nuxt-link>
        <nuxt-link to="/blog">Blog</nuxt-link>
        <nuxt-link to="/about">About</nuxt-link>
        <nuxt-link to="/contact">Contact</nuxt-link>

        <b-nav-item-dropdown text="Get Involved">
          <b-dropdown-item href="#"
            ><nuxt-link to="/getinvolved/volunteer"
              >Volunteer</nuxt-link
            ></b-dropdown-item
          >
          <b-dropdown-item href="#"
            ><nuxt-link to="/getinvolved/donate"
              >Donate</nuxt-link
            ></b-dropdown-item
          >
          <b-dropdown-item href="#"
            ><nuxt-link to="/getinvolved/fundraise"
              >Fundraise</nuxt-link
            ></b-dropdown-item
          >
        </b-nav-item-dropdown>
        <b-nav-item-dropdown text="Activities">
          <b-dropdown-item href="#"
            ><nuxt-link to="/activities/youthwork"
              >Youth Work</nuxt-link
            ></b-dropdown-item
          >
          <b-dropdown-item href="#"
            ><nuxt-link to="/activities/lunchboxgold"
              >Lunchbox Gold</nuxt-link
            ></b-dropdown-item
          >
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
.menu-bar {
  color: #fff;
}
.logo {
  width: 70px;
}
.navbar {
  /* position: fixed;
  width: 100%;
  top: 0; */
  z-index: 100;
  background-color: #172d4e !important;
}
.dropdown-menu {
  background-color: #3a78dc !important;
}
@media all and (min-width: 993px) {
  .navbar-collapse {
    justify-content: flex-end;
  }
  .navbar-nav {
    gap: 1.5rem;
  }
}
</style>
