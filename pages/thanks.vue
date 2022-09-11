<template>
  <div class="form-submission-thanks">
    <Navbar />
    <div class="section thanks-page-content">
      <h1>Thanks for submitting this form</h1>
      <NuxtLink to="/">
        <Button buttonContent="Back to home" />
      </NuxtLink>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
import Footer from "~/components/Footer.vue";
import Button from "~/components/Interaction/Button.vue";
export default { components: { Navbar, Footer, Button } };
</script>

<style>
.form-submission-thanks {
  display: flex;
  flex-direction: column;
  /* align-items: center; */
}
.form-submission-thanks h1 {
  text-align: center;
  padding: 10%;
}
.thanks-page-content {
  display: flex;
  flex-direction: column;
  width: 100%;
  align-items: center;
}
</style>
