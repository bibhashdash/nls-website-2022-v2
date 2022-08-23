<template>
  <div>
    <Navbar />
    <div class="profile-wrapper">
      <article>
        <NuxtLink to="/team"
          ><p style="color: #ff5e98; font-weight: bold">
            <span
              ><img
                src="../../assets/images/chevron_left_black_24dp.svg"
                alt=""
            /></span>
            Back to profiles
          </p></NuxtLink
        >
        <img
          class="profile-image"
          :src="require(`~/assets/images/${profile.img}`)"
          alt=""
        />
        <nuxt-content :document="profile" />
        <NuxtLink to="/team"
          ><b-button class="btn-primary back-to-all-profiles"
            >Back to all profiles</b-button
          ></NuxtLink
        >
      </article>
    </div>
  </div>
</template>

<script>
export default {
  name: "team-slug",
  async asyncData({ $content, params }) {
    const profile = await $content("teamProfiles", params.slug).fetch();

    return { profile };
  },
};
</script>

<style scoped>
.profile-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 5% 10%;
}
profile {
  width: 100%;
  max-width: 1000px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.profile-image {
  width: 100%;
  max-width: 800px;
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
</style>
