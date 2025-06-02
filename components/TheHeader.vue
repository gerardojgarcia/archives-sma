<script setup lang="ts">
import { ref } from 'vue'

const isOpen = ref(false)
const pagesOpen = ref(false)
</script>

<template>
<header class="fixed top-0 w-full bg-white z-10">

  <nav class="bg-white shadow-md">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <!-- Logo -->
        <div class="flex-shrink-0 flex items-center">
          <a href="#" class="flex items-center">
            <span class="inline-block w-8 h-8 bg-orange-300 rounded-b-full relative">
              <span class="absolute top-1 left-1 w-2 h-2 bg-teal-300 rounded-full"></span>
              <span class="absolute top-1 right-1 w-2 h-2 bg-teal-300 rounded-full"></span>
            </span>
            <span class="ml-2 text-xl font-semibold">ArchivistaSMA</span>
          </a>
        </div>
        <!-- Desktop Menu -->
        <div class="hidden md:flex md:items-center md:space-x-6">
          <a href="#" class="text-gray-700 font-medium">Home</a>
          <a href="#about" class="text-gray-700 hover:text-gray-900 active:text-blue-900">About Us</a>
          <a href="#" class="text-gray-700 hover:text-gray-900">Services</a>
          <a href="#" class="text-gray-700 hover:text-gray-900">Projects</a>


          <a href="#contact" class="ml-4 inline-flex items-center px-4 py-2 bg-black text-white rounded-full hover:bg-gray-800">
            Contact
            <span class="ml-2 inline-flex items-center justify-center w-4 h-4 bg-white text-black rounded-full">+</span>
          </a>
        </div>
        <!-- Mobile hamburger -->
        <div class="flex items-center md:hidden">
          <button @click="isOpen = !isOpen" class="inline-flex items-center justify-center p-2 rounded-md text-gray-700 hover:text-gray-900 focus:outline-none">
            <svg v-if="!isOpen" class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
            <svg v-else class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>
    </div>
    <!-- Mobile Menu -->
    <div v-if="isOpen" class="md:hidden">
      <div class="px-2 pt-2 pb-3 space-y-1">
        <a href="#" class="block px-3 py-2 text-purple-600 font-medium">Home</a>
        <a href="#" class="block px-3 py-2 text-gray-700 hover:bg-gray-100 rounded-md">About Us</a>
        <a href="#services" class="block px-3 py-2 text-gray-700 hover:bg-gray-100 rounded-md">Services</a>
        <a href="#" class="block px-3 py-2 text-gray-700 hover:bg-gray-100 rounded-md">Projects</a>
        <div class="border-t border-gray-200"></div>


        <a href="#" class="block mt-2 px-3 py-2 bg-black text-white text-center rounded-full hover:bg-gray-800">Get Started +</a>
      </div>
    </div>
  </nav>
  
</header>
</template>

<style scoped>

</style>