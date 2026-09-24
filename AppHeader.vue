<template>
  <header class="site-header">
    <h1 class="title">Explore Places</h1>
    <p class="subtitle">Your personal guide to memorable journeys</p>

    <nav class="nav-bar">
      <button @click="$emit('change-view', 'Home')">Home</button>
      <button @click="$emit('change-view', 'Destination')">Destinations</button>
      <button @click="$emit('change-view', 'Contact')">Contact</button>
    </nav>
  </header>
</template>

<style scoped>
/* Header background matches Task 6.3D */
.site-header {
  background-color: #000000;
  color: #FFFFFF;
  text-align: center;
  padding: 1.5rem 5%;
  font-family: "Montserrat", sans-serif;
}

.title {
  margin: 0;
  font-size: 2rem;
}

.subtitle {
  margin: 0.3rem 0 1rem;
  font-family: "Lato", sans-serif;
}

.nav-bar {
  background-color: #1E88E5;
  padding: 1rem;
  display: flex;
  justify-content: center;
  gap: 1rem;
  flex-wrap: wrap;
}

.nav-bar button {
  background: none;
  border: none;
  color: #FFFFFF;
  font-weight: bold;
  font-family: "Lato", sans-serif;
  padding: 0.5rem 1rem;
  cursor: pointer;
  font-size: 1rem;
}

.nav-bar button:hover {
  text-decoration: underline;
}

/* responsive design */ 
@media (max-width: 768px) {
  .nav-bar {
    flex-direction: column;
  }

  .nav-bar button {
    width: 100%;
    text-align: center;
  }
}
</style>
