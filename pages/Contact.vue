<template>
  <div>
    <Navbar />
    <section class="secondary-hero">
      <h1>Contact Us</h1>
    </section>
    <section class="section section-form">
      <form
        class="form"
        action="/thanks"
        name="contactus"
        method="post"
        netlify
        netlify-honeypot="bot-field"
      >
        <input type="hidden" name="form-name" value="contactus" />
        <label for="name">Name</label>
        <input name="name" type="text" />
        <label for="message">Message</label>
        <textarea name="message" id="" cols="30" rows="10"></textarea>
        <button type="submit" class="btn-primary">Submit</button>
      </form>
    </section>
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
export default {
  components: { Navbar },
};
</script>

<style>
.secondary-hero {
  background: linear-gradient(
      to right,
      rgba(50, 70, 80, 0.55),
      rgba(50, 70, 80, 0.55)
    ),
    url("../assets/images/secondary-hero.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: 15% 5%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  color: #fff;

  font-weight: 800;

  text-shadow: 0px 0px 9px #000000;
}
.secondary-hero h1 {
  font-size: 3rem;
}
.form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  padding: 5%;
}
input,
textarea {
  border-radius: 10px;
  border: 2px solid rgb(171, 171, 171);
}
@media all and (min-width: 481px) and (max-width: 576px) {
  .secondary-hero {
    padding: 10% 5%;
  }
  .secondary-hero h1 {
    font-size: 4rem;
  }
}
@media all and (min-width: 577px) and (max-width: 768px) {
  .secondary-hero {
    padding: 8% 5%;
  }
  .secondary-hero h1 {
    font-size: 4rem;
  }
}
@media all and (min-width: 769px) and (max-width: 992px) {
  .secondary-hero {
    padding: 8% 5%;
  }
  .secondary-hero h1 {
    font-size: 4rem;
  }
}
@media all and (min-width: 992px) {
  .secondary-hero {
    padding: 8% 5%;
    background-position: center;
  }
  .secondary-hero h1 {
    font-size: 5rem;
  }
}
</style>
