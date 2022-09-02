<template>
  <div class="footer">
    <div class="footer-main-content">
      <div class="footer-item footer-charity-info">
        <div class="footer-charity-brand">
          <img
            class="logo"
            src="../assets/images/NLS_round_logo_gold.png"
            alt=""
          />
          <h3>New Life Support</h3>
        </div>
        <div class="footer-charity-info-text">
          <p>
            New Life Support is a registered charity in England and Wales
            (Charity number: 1156235). For a full list of our financial and
            annual reports please visit the Charities Commission website by
            clicking here.
          </p>
        </div>
      </div>
      <div class="footer-item footer-contact-info">
        <h3>Contact</h3>
        <div class="contact-info-item">
          <img src="../assets/images/email-icon.svg" alt="" />
          <p>support@revivechurch.co.uk</p>
        </div>
        <div class="contact-info-item">
          <img src="../assets/images/telephone-icon.svg" alt="" />
          <p>07947 013960</p>
        </div>
      </div>
      <div class="footer-item footer-address">
        <h3>Find us</h3>
        <div class="address-info-item">
          <p>Revive Church</p>

          <p>Mariners Street, Goole</p>

          <p>DN14 5DH</p>
        </div>
      </div>
    </div>
    <div class="footer-secondary-content">
      <p>Copyright 2022 New Life Support</p>
      <p>Website design by <span>NINE BLOCK MEDIA</span></p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.footer {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.footer h3,
.footer p {
  color: #fff;
}
.footer h3 {
  border-bottom: 3px solid #ff5e98;
  width: fit-content;
  padding-bottom: 0.2rem;
}
.footer p {
  font-size: 0.8rem;
  margin: 0;
}

.footer-main-content {
  padding: 10% 5%;
  display: flex;
  flex-direction: column;
  gap: 3rem;
  background-color: #202020;
}
/* .footer-charity-brand {
  display: flex;
} */

.contact-info-item {
  display: flex;
  flex-direction: row;
  gap: 1rem;
  align-items: center;
  /* border: 1px solid white; */
  margin: 0.5rem 0;
}
.footer-secondary-content {
  background-color: #fff;
  color: #202020;
  padding: 0.5rem 0;
}
.footer-secondary-content p {
  color: #202020;
  font-size: 0.6rem;
  text-align: center;
  font-weight: bold;
}
.footer-secondary-content span {
  color: rgb(28, 182, 182);
}

@media all and (min-width: 576px) and (max-width: 768px) {
  .footer-main-content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    padding: 4% 15%;
    justify-items: center;
  }
  .footer-charity-info {
    grid-column: 1 / span 2;
  }
}
@media all and (min-width: 769px) and (max-width: 992px) {
  .footer-main-content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    padding: 4% 15%;
    justify-items: center;
  }
  .footer-charity-info {
    grid-column: 1 / span 2;
  }
}
@media all and (min-width: 993px) {
  .footer-main-content {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    padding: 4% 10%;
    justify-items: center;
  }
}
@media all and (min-width: 1201px) {
  .footer-main-content {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    padding: 4% 20%;
    justify-items: center;
  }
}
</style>
