<template>
  <section class="contact-form">
    <h2>{{ formTitle }}</h2>

    <form @submit.prevent="submitForm">
      <!-- First Name -->
      <label>
        First Name:
        <input
          type="text"
          v-model="form.firstName"
          required
        >
      </label>

      <!-- Last Name input -->
      <label>
        Last Name:
        <input
          type="text"
          v-model="form.lastName"
          required
        >
      </label>

      <!-- Email input field -->
      <label>
        Email:
        <input
          type="email"
          v-model="form.email"
          required
        >
      </label>

      <!-- Phone input field -->
      <label>
        Phone:
          <input
           type="tel"
           v-model="form.phone" required
           inputmode="numeric"
           pattern="[0-9]*"
           >
      </label>

      <!-- Destination Dropdown list -->
      <label>
        Destination:
        <select v-model="form.destination" required>
          <option disabled value="">Select a destination</option>
          <option
            v-for="place in destinations"
            :key="place"
            :value="place"
          >
            {{ place }}
          </option>
        </select>
      </label>

      <!-- Subject input field -->
      <label>
        Subject:
        <input
          type="text"
          v-model="form.subject"
          required
        >
      </label>

      <!-- Description input field -->
      <label>
        Description:
        <textarea
          v-model="form.description"
          rows="4"
          required
        ></textarea>
      </label>

      <button type="submit" class="submit-btn">Submit</button>
      <button type="button" class="reset-btn" @click="resetForm">Reset</button>

    </form>
  </section>
</template>

<script setup>
import { ref } from 'vue'

// defineProps
const props = defineProps({
  formTitle: {
    type: String,
    default: 'Contact Form'
  }
})

// defineEmits
const emit = defineEmits(['submit-form'])

// Form data
const form = ref({
  firstName: '',
  lastName: '',
  email: '',
  phone: null,
  destination: '',
  subject: '',
  description: ''
})

// Dropdown list element
const destinations = [
  'Gold Coast',
  'Singapore',
  'New York'
]

// Form submission handler
function submitForm() {
  // Emit shallow copy
  emit('submit-form', { ...form.value })

// Form reset button
  function resetForm() {
  form.value = {
    firstName: "",
    lastName: "",
    email: "",
    phone: "",
    destination: "",
    subject: "",
    description: ""
  }
}

  // Resets the form after 2 seconds
  setTimeout(() => {
    form.value = {
      firstName: '',
      lastName: '',
      email: '',
      phone: "",
      destination: '',
      subject: '',
      description: ''
    }
  }, 2000)
}
</script>

<style scoped>
.contact-form {
  max-width: 600px;
  margin: 2rem auto;
  padding: 2rem;
  background-color: #F2F2F2;
  border-radius: 0.5rem;
  font-family: "Lato", sans-serif;
}

h2 {
  text-align: center;
  font-family: "Montserrat", sans-serif;
  margin-bottom: 1.5rem;
}

form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

label {
  display: flex;
  flex-direction: column;
  font-weight: bold;
}

input,
select,
textarea {
  margin-top: 0.3rem;
  padding: 0.6rem;
  border-radius: 0.3rem;
  border: 1px solid #ccc;
}

.submit-btn {
  background-color: #1E88E5;
  color: #fff;
  padding: 0.8rem;
  border: none;
  border-radius: 0.3rem;
  font-weight: bold;
  cursor: pointer;
}

.submit-btn:hover {
  background-color: #1565C0;
}

.reset-btn {
  background-color: #eb3b3b;
  color: #FFFFFF;
  padding: 0.8rem;
  border: none;
  border-radius: 0.3rem;
  font-weight: bold;
  cursor: pointer; 
  font-family: "Lato", sans-serif;
}

.reset-btn:hover {
  background-color: #880808;
}

</style>
