<template>
  <section class="intro">
    <h2>Discover Your Next Destination</h2>
    <p>
      Exploring beautiful destinations, local experiences, cuisine and travel tips to help you
      plan your next journey.
    </p>

    <button class="button">Explore Destinations</button>
  </section>

  <section class="destinations">
    <h2>Popular Destinations</h2>

    <div class="cards">
      <div class="card">
        <img src="/GoldCoast.jpg" alt="Gold Coast">
        <h3>Gold Coast</h3>
        <p>Beautiful beaches, theme parks and vibrant coastal life.</p>
      </div>

      <div class="card">
        <img src="/Singapore.jpg" alt="Singapore">
        <h3>Singapore</h3>
        <p>Modern attractions, gardens and diverse cultural experiences.</p>
      </div>

      <div class="card">
        <img src="/NYC.jpg" alt="New York">
        <h3>New York</h3>
        <p>Iconic landmarks, rich culture and unforgettable city life.</p>
      </div>
    </div>
  </section>

  <section class="travel-guide">
    <h2>Plan Your Journey</h2>

    <div class="guide-content">
      <div>
        <h3>Travel Tips</h3>
        <p>Find reliable information to make your journey easier and more enjoyable.</p>
      </div>

      <div>
        <h3>Local Experiences</h3>
        <p>Discover local cuisine, culture and activities to enhance your trip.</p>
      </div>

      <div>
        <h3>Budget Planning</h3>
        <p>Explore travel options that help you plan a trip suitable for your budget.</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Introduction */
.intro {
  text-align: center;
  padding: 4rem 5%;
  font-family: "Lato", sans-serif;
}

.intro h2 {
  font-family: "Montserrat", sans-serif;
  font-size: 2rem;
  margin-bottom: 1rem;
}

.button {
  display: inline-block;
  background-color: #1E88E5;
  color: #fff;
  padding: 0.8rem 1.5rem;
  border-radius: 0.3rem;
  font-weight: bold;
  border: none;
  cursor: pointer;
}

.button:hover {
  background-color: #1565C0;
}

/* Popular Destinations */
.destinations {
  padding: 2rem 0;
  text-align: center;
}

.cards {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  padding: 1rem;
}

.card {
  border: 1px solid #ccc;
  padding: 1rem;
  border-radius: 0.5rem;
  background-color: #fff;
}

.card img {
  width: 100%;
  border-radius: 0.3rem;
}

.card h3 {
  font-family: "Montserrat", sans-serif;
}

/* Travel Guidance section */
.travel-guide {
  padding: 2rem 0;
  text-align: center;
}

.guide-content {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.guide-content div {
  background-color: #f2f2f2;
  padding: 1.5rem;
  border-radius: 0.5rem;
}

@media (min-width: 768px) {
  .cards {
    flex-direction: row;
  }

  .card {
    width: 33%;
  }

  .guide-content {
    flex-direction: row;
  }

  .guide-content div {
    width: 33%;
  }
}
</style>
