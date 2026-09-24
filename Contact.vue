<template>
  <section class="contact-section">
    <h2>Contact Us</h2>
    <p class="contact-intro">
      Need help planning your journey? We’re here to assist with any questions or travel advice.
    </p>

    <div class="contact-info">
      <div>
        <h3>Email</h3>
        <p>exploreplaces@gmail.com</p>
      </div>

      <div>
        <h3>Phone</h3>
        <p>+61 000 111 222</p>
      </div>

      <div>
        <h3>Business Hours</h3>
        <p>Mon – Fri: 9 AM – 5 PM</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact-section {
  text-align: center;
  padding: 3rem 5%;
  font-family: "Lato", sans-serif;
}

.contact-section h2 {
  font-family: "Montserrat", sans-serif;
  margin-bottom: 0.5rem;
}

.contact-intro {
  max-width: 600px;
  margin: 0 auto 2rem;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.contact-info div {
  background-color: #F2F2F2;
  padding: 1.5rem;
  border-radius: 0.5rem;
}

.contact-info h3 {
  font-family: "Montserrat", sans-serif;
  margin-bottom: 0.3rem;
}

@media (min-width: 768px) {
  .contact-info {
    flex-direction: row;
    justify-content: center;
  }

  .contact-info div {
    width: 30%;
  }
}
</style>
