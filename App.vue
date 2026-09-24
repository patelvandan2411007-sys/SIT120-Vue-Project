<template>
  <div>
    <!-- header -->
    <AppHeader @change-view="currentView = $event" />

    <!-- Dynamic page rendering -->
    <component :is="views[currentView]" />

    <!-- Contact form  -->
    <ContactForm
      v-if="currentView === 'Contact'"
      formTitle="Contact Us"
      @submit-form="handleFormSubmit"
    />

    <!-- Acknowledgement card -->
    <section v-if="submittedData" class="ack-card">
      <h3>Customer Acknowledgement</h3>
      <p>Thank you for your enquiry! Here are your details:</p>
      <ul>
        <li><strong>Name:</strong> {{ submittedData.firstName }} {{ submittedData.lastName }}</li>
        <li><strong>Email:</strong> {{ submittedData.email }}</li>
        <li><strong>Phone:</strong> {{ submittedData.phone }}</li>
        <li><strong>Destination:</strong> {{ submittedData.destination }}</li>
        <li><strong>Subject:</strong> {{ submittedData.subject }}</li>
        <li><strong>Description:</strong> {{ submittedData.description }}</li>
      </ul>
    </section>

    <!-- Footer -->
    <AppFooter />
  </div>
</template>

<script setup>
import { ref } from 'vue'

import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'

import Home from './components/Home.vue'
import Destination from './components/Destination.vue'
import Contact from './components/Contact.vue'
import ContactForm from './components/ContactForm.vue'

const currentView = ref('Home')
const submittedData = ref(null)

const views = {
  Home,
  Destination,
  Contact
}

function handleFormSubmit(data) {
  submittedData.value = data
}
</script>

<style>
.ack-card {
  background: #f2f2f2;
  padding: 1.5rem;
  margin: 2rem auto;
  width: 80%;
  border-radius: 8px;
}
</style>
