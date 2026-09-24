<template>
  <!-- Destination Intro -->
  <section class="destination-intro">
    <img src="/GoldCoast.jpg" alt="Gold Coast">

    <div class="intro-text">
      <h2>Explore Gold Coast</h2>
      <p>
        Explore one of the most beautiful, charming and exciting coastal cities. Enjoy beaches,
        theme parks, local food and plenty of activities for all kinds of travellers.
      </p>
    </div>
  </section>

  <!-- Destination Details -->
  <section class="destination-details">
    <h2>Travel Guide</h2>

    <div class="detail-content">
      <div>
        <h3>Popular Attractions</h3>
        <p>
          Visit Surfers Paradise, Burleigh Heads, Broadbeach and other scenic spots. The Gold Coast
          is known for its beaches, nightlife and adventure activities.
        </p>
      </div>

      <div>
        <h3>Local Cuisine</h3>
        <p>
          Enjoy beachfront restaurants, cafes and food markets offering fresh seafood and a mix of
          international flavours.
        </p>
      </div>

      <div>
        <h3>Accommodation</h3>
        <p>
          Choose from hotels, beachside resorts, apartments and budget-friendly stays depending on
          your travel style.
        </p>
      </div>

      <div>
        <h3>Getting Around</h3>
        <p>
          The city offers buses, trams, taxis and other transport services that make it easy to move
          around popular tourist areas.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.destination-intro {
  padding: 2rem 0;
}

.destination-intro img {
  width: 100%;
  border-radius: 0.5rem;
}

.intro-text {
  padding: 1rem 0;
  text-align: center;
}

.intro-text h2 {
  font-family: "Montserrat", sans-serif;
}

.destination-details {
  padding: 2rem 0;
  text-align: center;
}

.detail-content {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-top: 1rem;
}

.detail-content div {
  background-color: #F2F2F2;
  padding: 1.5rem;
  border-radius: 0.5rem;
  text-align: left;
}

@media (min-width: 768px) {
  .destination-intro {
    display: flex;
    align-items: center;
    gap: 2rem;
  }

  .destination-intro img,
  .intro-text {
    width: 50%;
  }

  .detail-content {
    flex-direction: row;
    flex-wrap: wrap;
  }

  .detail-content div {
    width: 48%;
  }
}
</style>
