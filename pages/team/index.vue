<template>
  <div>
    <Navbar />
    <SecondaryHero mainTitle="Our Team" />
    <section class="section section-team">
      <h2>Profiles</h2>
      <ul class="profiles-grid">
        <li v-for="profile of teamProfiles" :key="profile.slug">
          <img
            class="team-profile-image"
            :src="require(`~/assets/images/teamImages/${profile.img}`)"
            alt=""
          />
          <NuxtLink
            :to="{
              name: 'team-slug',
              params: {
                slug: profile.slug,
              },
            }"
          >
            <p class="profile-title">
              {{ profile.title }}
              <span
                ><img
                  src="../../assets/images/chevron_right_white_24dp.svg"
                  alt=""
              /></span>
            </p>
          </NuxtLink>

          <p class="profile-role">{{ profile.role }}</p>
        </li>
      </ul>
    </section>
    <Footer />
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
import Footer from "~/components/Footer.vue";
import SecondaryHero from "~/components/SecondaryHero.vue";
export default {
  components: { Navbar, Footer, SecondaryHero },
  async asyncData({ $content }) {
    const teamProfiles = await $content("teamProfiles").fetch();

    return { teamProfiles };
  },
};
</script>

<style>
ul,
li {
  list-style: none;
  padding: 0;
  margin: 0;
}
.section-team-grid {
  padding: 5%;
}
.section-team-grid h2 {
  color: #ff5e98;
  font-weight: bold;
  text-decoration: underline;
  text-align: center;
  margin-bottom: 2rem;
}
.profiles-grid {
  display: grid;
  grid-template-columns: auto;
}
.team-profile-image {
  width: 100%;
}
.profile-title {
  background-color: #ff5e98;
  color: white;
  font-weight: bold;
  font-size: 1.5rem;
  margin-bottom: 0;
  width: fit-content;
  padding: 2px 10px;
}
.profile-role {
  background-color: black;
  color: white;
  width: fit-content;
  font-size: 1rem;
  font-weight: bold;
  padding: 2px 10px;
}

@media all and (min-width: 577px) {
  .profiles-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }
}
@media all and (min-width: 993px) {
  .profiles-grid {
    gap: 2rem;
    padding: 5% 10%;
  }
}
</style>
