<template>
  <div>
    <Navbar />
    <div class="profile-wrapper">
      <article class="profile-item-container">
        <img
          class="profile-full-post-image"
          :src="require(`~/assets/images/teamImages/${profile.img}`)"
          alt=""
        />
        <div class="profile-content">
          <nuxt-content :document="profile" />
          <NuxtLink to="/team">
            <Button buttonContent="Back to all profiles" />
          </NuxtLink>
        </div>
      </article>
    </div>
    <Footer />
  </div>
</template>

<script>
import Button from "~/components/Interaction/Button.vue";
import Footer from "~/components/Footer.vue";
export default {
  name: "team-slug",
  async asyncData({ $content, params }) {
    const profile = await $content("teamProfiles", params.slug).fetch();
    return { profile };
  },
  components: { Button, Footer },
};
</script>

<style scoped>
.profile-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 5% 10%;
}
.profile-item-container {
  display: grid;
  grid-template-columns: auto;
  place-items: center;
  width: 100%;
}
.profile-full-post-image {
  width: 100%;
  max-width: 300px;
}
.profile-wrapper a {
  align-self: flex-start;
}
.back-to-all-profile {
  width: 150px;
  border-radius: 20px;
  background-color: #ff5e98;
  border: none;
  padding: 5px 0;
}

@media all and (min-width: 768px) {
  .profile-item-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
    width: 80%;
  }
}
</style>
