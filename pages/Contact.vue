<template>
  <div>
    <Navbar />
    <SecondaryHero mainTitle="Contact Us" />
    <section class="section section-form-info">
      <form
        class="form"
        action="/thanks"
        name="contactus"
        method="post"
        netlify
        netlify-honeypot="bot-field"
      >
        <h2>Write to us</h2>
        <input type="hidden" name="form-name" value="contactus" />
        <div class="form-item">
          <label for="name">Name:</label>
          <input
            name="name"
            type="text"
            required
            placeholder="This is a required field"
          />
        </div>
        <div class="form-item">
          <label for="email">Email:</label>
          <input
            name="email"
            type="email"
            placeholder="If you require a response"
          />
        </div>
        <div class="form-item">
          <label for="subject">Subject:</label>
          <input
            name="subject"
            type="text"
            required
            placeholder="This is a required field"
          />
        </div>
        <div class="form-item">
          <label for="message">Message:</label>
          <textarea
            name="message"
            id=""
            cols="30"
            rows="10"
            required
            placeholder="This is a required field"
          ></textarea>
        </div>

        <button type="submit" class="btn-primary form-submit">Submit</button>
      </form>
      <div class="contact-info">
        <h2>Contact Info</h2>
        <div class="contact-info-item">
          <p><b>Email:</b> support@revivechurch.co.uk</p>
        </div>
        <div class="contact-info-item">
          <p><b> Telephone:</b> 07947 013960</p>
        </div>
        <div class="address-info-item">
          <p>
            <b> Address:</b> <br />
            Revive Church <br />Mariners Street, Goole <br />DN14 5DH
          </p>
        </div>
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d702.1647005683946!2d-0.87457403533561!3d53.7041678000595!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x48791f091d667a9d%3A0x470ebf39e4655078!2sRevive%20Church!5e0!3m2!1sen!2suk!4v1660852990833!5m2!1sen!2suk"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          class="google-maps-pin"
        ></iframe>
      </div>
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
};
</script>

<style>
.section-form-info {
  display: grid;
  grid-template-columns: auto;
  gap: 2rem;
}
.section-form-info h2 {
  color: #ff5e98;
  font-weight: bold;
  text-decoration: underline;
  text-align: center;
  margin-bottom: 2rem;
}
.form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  padding: 5%;
  width: 100%;
}
.contact-info {
  padding: 5%;
}
.form-item {
  display: flex;
  flex-direction: column;
}
label {
  margin: 0;
}
input,
textarea {
  border-radius: 10px;
  border: 2px solid rgb(171, 171, 171);
}
input {
  padding: 10px;
}
.form-submit {
  align-self: center;

  width: 150px;
  border-radius: 20px;
  background-color: #ff5e98;
  border: none;
  padding: 5px 0;
}
.google-maps-pin {
  width: 100%;
  height: 400px;
}

@media all and (min-width: 769px) and (max-width: 992px) {
  .section-form-info {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    padding: 5% !important;
    /* gap: 2rem; */
  }
}
@media all and (min-width: 992px) {
  .section-form-info {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    padding: 5% !important;
    /* gap: 2rem; */
  }
}
@media all and (min-width: 1200px) {
  .section-form-info {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    padding: 10% !important;
    /* gap: 2rem; */
  }
}
</style>
