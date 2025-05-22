<script setup lang="ts">
import { ref } from 'vue'

const newsletterEmail = ref('')

function subscribe() {
  console.log('Subscribed email:', newsletterEmail.value)
  newsletterEmail.value = ''
}
</script>

<template>
  <footer class="bg-white border-t mt-16">
    <div class="container mx-auto px-6 lg:px-8 py-12">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
        <!-- Brand & Newsletter -->
        <div class="lg:col-span-2">
          <!-- Logo -->
          <div class="flex items-center mb-4">
            <span class="inline-block w-8 h-8 bg-orange-300 rounded-b-full relative">
              <span class="absolute top-1 left-1 w-2 h-2 bg-teal-300 rounded-full"></span>
              <span class="absolute top-1 right-1 w-2 h-2 bg-teal-300 rounded-full"></span>
            </span>
            <span class="ml-2 text-2xl font-semibold text-gray-900">ArchivistaSMA</span>
          </div>
          <!-- Description -->
          <p class="text-gray-600 mb-6">
            Partner with us for innovative digital marketing solutions that
            drive growth, increase engagement, and elevate your brand's success.
          </p>
          <!-- Newsletter -->
          <h4 class="text-lg font-semibold text-gray-900 mb-2">Newsletter</h4>
          <p class="text-gray-600 mb-4">
            Stay updated with our latest digital marketing insights!
          </p>
          <div class="flex max-w-md bg-gray-50 rounded-full overflow-hidden">
            <input
                v-model="newsletterEmail"
                type="email"
                placeholder="Enter your Email"
                class="flex-1 px-4 py-3 bg-transparent focus:outline-none"
            />
            <button
                @click="subscribe"
                class="px-6 bg-purple-600 text-white font-medium hover:bg-purple-500 transition"
            >
              Send
            </button>
          </div>
        </div>

        <!-- Quick Links -->
        <div>
          <h4 class="text-lg font-semibold text-gray-900 mb-4">Quick Link</h4>
          <ul class="space-y-2 text-gray-600">
            <li><a href="#" class="hover:text-gray-900">Home</a></li>
            <li><a href="#" class="hover:text-gray-900">About Us</a></li>
            <li><a href="#" class="hover:text-gray-900">Services</a></li>
            <li><a href="#" class="hover:text-gray-900">Projects</a></li>
            <li><a href="#" class="hover:text-gray-900">Team</a></li>

            <li><a href="#" class="hover:text-gray-900">Contact</a></li>
          </ul>
        </div>

        <!-- Services
        <div>
          <h4 class="text-lg font-semibold text-gray-900 mb-4">Services</h4>
          <ul class="space-y-2 text-gray-600">
            <li><a href="#" class="hover:text-gray-900">Artwork Cataloging</a></li>
            <li><a href="#" class="hover:text-gray-900">Condition Reporting</a></li>
            <li><a href="#" class="hover:text-gray-900">Digitization Services</a></li>
            <li><a href="#" class="hover:text-gray-900">Conservation Consulting</a></li>
            <li><a href="#" class="hover:text-gray-900">Exhibition Coordination</a></li>
            <li><a href="#" class="hover:text-gray-900">Archival Storage Solutions</a></li>
          </ul>
        </div> -->

        <!-- Utility Pages
        <div>
          <h4 class="text-lg font-semibold text-gray-900 mb-4">Utility Pages</h4>
          <ul class="space-y-2 text-gray-600">
            <li><a href="#" class="hover:text-gray-900">Style Guide</a></li>
            <li><a href="#" class="hover:text-gray-900">Licenses</a></li>
            <li><a href="#" class="hover:text-gray-900">Changelog</a></li>
            <li><a href="#" class="hover:text-gray-900">Protected</a></li>
            <li><a href="#" class="hover:text-gray-900">Not Found</a></li>
          </ul>
        </div> -->

        <!-- Contact Us -->
        <div>
          <h4 class="text-lg font-semibold text-gray-900 mb-4">Contact Us</h4>
          <ul class="space-y-4 text-gray-600">
            <li class="flex items-center">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-3 text-gray-900" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5h2l.4 2M7 13l-2 2m4-2l1.5 1.5M17 13l2 2m-4-2l-1.5 1.5M21 5h-2l-.4 2M7 5h10M7 3h10a2 2 0 012 2v2a2 2 0 01-2 2H7a2 2 0 01-2-2V5a2 2 0 012-2z" />
              </svg>
              <span>(415) 555-1234</span>
            </li>
            <li class="flex items-center">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-3 text-gray-900" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 12H8m8 0l-4 4m4-4l-4-4m6 4a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
              <span>info@archivalservices.com</span>
            </li>
            <li class="flex items-center">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-3 text-gray-900" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 11c1.657 0 3-1.343 3-3S13.657 5 12 5s-3 1.343-3 3 1.343 3 3 3zm0 8c-4.418 0-8-3.582-8-8 0-4.418 3.582-8 8-8s8 3.582 8 8c0 4.418-3.582 8-8 8z" />
              </svg>
              <span>San Miguel de Allende, MX</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>

</style>