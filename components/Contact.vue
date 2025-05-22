<script setup lang="ts">
import { reactive } from 'vue'

const form = reactive({
  firstName: '',
  lastName: '',
  email: '',
  message: ''
})

function onSubmit() {
  // handle form submission
  console.log('Form submitted:', form)
  // reset form
  form.firstName = ''
  form.lastName = ''
  form.email = ''
  form.message = ''
}
</script>

<template>
  <section class="py-16 bg-white" id="contact">
    <div class="container mx-auto px-6 lg:px-8">
      <!-- Header -->
      <h2 class="text-center text-4xl font-bold mb-2">Let's Talk Now</h2>
      <p class="text-center text-gray-600 mb-8">
        Helping you preserve and showcase your art with professional archival services.
      </p>

      <!-- Contact Cards -->
      <div class="grid gap-6 md:grid-cols-3 mb-12">
        <div class="flex items-center bg-gray-50 p-6 rounded-2xl">
          <div class="p-3 bg-purple-100 rounded-full mr-4">
            <!-- Email Icon -->
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M16 12H8m8 0l-4 4m4-4l-4-4m6 4a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </div>
          <div>
            <h5 class="text-lg font-semibold text-gray-900">Email Us</h5>
            <p class="text-gray-600">info@archivalservices.com</p>
          </div>
        </div>
        <div class="flex items-center bg-gray-50 p-6 rounded-2xl">
          <div class="p-3 bg-purple-100 rounded-full mr-4">
            <!-- Phone Icon -->
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M3 5h2l.4 2M7 13l-2 2m4-2l1.5 1.5M17 13l2 2m-4-2l-1.5 1.5M21 5h-2l-.4 2M7 5h10M7 3h10a2 2 0 012 2v2a2 2 0 01-2 2H7a2 2 0 01-2-2V5a2 2 0 012-2z" />
            </svg>
          </div>
          <div>
            <h5 class="text-lg font-semibold text-gray-900">Call Us</h5>
            <p class="text-gray-600">(415) 555-1234</p>
          </div>
        </div>
        <div class="flex items-center bg-gray-50 p-6 rounded-2xl">
          <div class="p-3 bg-purple-100 rounded-full mr-4">
            <!-- Location Icon -->
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M12 11c1.657 0 3-1.343 3-3S13.657 5 12 5s-3 1.343-3 3 1.343 3 3 3zm0 8c-4.418 0-8-3.582-8-8 0-4.418 3.582-8 8-8s8 3.582 8 8c0 4.418-3.582 8-8 8z" />
            </svg>
          </div>
          <div>
            <h5 class="text-lg font-semibold text-gray-900">Location</h5>
            <p class="text-gray-600">San Miguel de Allende, MX</p>
          </div>
        </div>
      </div>

      <!-- Contact Form -->
      <div class="bg-gray-50 p-8 rounded-2xl">
        <form @submit.prevent="onSubmit" class="space-y-6">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <input
                v-model="form.firstName"
                type="text"
                placeholder="First Name"
                class="w-full p-4 bg-white rounded-xl border border-gray-200 focus:outline-none focus:ring-2 focus:ring-purple-400"
            />
            <input
                v-model="form.lastName"
                type="text"
                placeholder="Last Name"
                class="w-full p-4 bg-white rounded-xl border border-gray-200 focus:outline-none focus:ring-2 focus:ring-purple-400"
            />
          </div>
          <input
              v-model="form.email"
              type="email"
              placeholder="Enter email address"
              class="w-full p-4 bg-white rounded-xl border border-gray-200 focus:outline-none focus:ring-2 focus:ring-purple-400"
          />
          <textarea
              v-model="form.message"
              rows="5"
              placeholder="Enter Your Message"
              class="w-full p-4 bg-white rounded-xl border border-gray-200 focus:outline-none focus:ring-2 focus:ring-purple-400"
          ></textarea>
          <button
              type="submit"
              class="px-8 py-4 bg-purple-600 text-white rounded-full hover:bg-purple-500 transition"
          >
            Submit
          </button>
        </form>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>