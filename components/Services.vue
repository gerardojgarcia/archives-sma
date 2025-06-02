<script setup lang="ts">
const services = [
  {
    title: 'Artwork Cataloging',
    description:
        'Comprehensive inventory and metadata creation for artworks, including provenance and exhibition history.',
    icon: '📦',
    bgClass: 'bg-yellow-50',
    shapeBg: 'bg-yellow-100'
  },
  {
    title: 'Condition Reporting',
    description:
        'Detailed assessments and photographic documentation of artwork condition to inform preservation decisions.',
    icon: '📝',
    bgClass: 'bg-blue-50',
    shapeBg: 'bg-blue-100'
  },
  {
    title: 'Digitization Services',
    description:
        'High‑resolution scanning and digital archiving of sketches, diaries, and original artworks for long‑term access.',
    icon: '📷',
    bgClass: 'bg-green-50',
    shapeBg: 'bg-green-100'
  },
  {
    title: 'Conservation Consulting',
    description:
        'Expert guidance on preventive care, environmental controls, and best practices for artwork preservation.',
    icon: '🛡️',
    bgClass: 'bg-purple-50',
    shapeBg: 'bg-purple-100'
  },
  {
    title: 'Exhibition Coordination',
    description:
        'Planning and support for exhibit installations, label creation, and display guidelines tailored to each project.',
    icon: '🖼️',
    bgClass: 'bg-pink-50',
    shapeBg: 'bg-pink-100'
  },
  {
    title: 'Archival Storage Solutions',
    description:
        'Custom archival‐quality housing and secure storage recommendations to ensure long‑term safety of collections.',
    icon: '📂',
    bgClass: 'bg-indigo-50',
    shapeBg: 'bg-indigo-100'
  }
]
</script>

<template>
  <section class="py-16 bg-white" id="services">
    <div class="container mx-auto px-6 lg:px-8">
      <!-- Header -->
      <div class="flex justify-between items-center mb-8">
        <h2 class="text-3xl font-bold text-gray-900">Our Artist Archival Services</h2>
        <button class="px-5 py-2 bg-purple-600 text-white rounded-full inline-flex items-center hover:bg-purple-500 transition">
          Get Started
          <span class="ml-2 inline-flex items-center justify-center w-5 h-5 bg-white text-purple-600 rounded-full">+</span>
        </button>
      </div>
      <!-- Services Grid -->
      <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
        <div
            v-for="service in services"
            :key="service.title"
            :class="service.bgClass + ' p-6 rounded-2xl shadow-sm transition-shadow duration-200 ease-in-out hover:shadow-lg' ">
          <div class="relative mb-4 w-12 h-12">
            <div
                class="absolute inset-0 rounded-xl transform rotate-6"
                :class="service.shapeBg">
            </div>
            <div class="relative flex items-center justify-center w-full h-full">
              <span class="text-xl">{{ service.icon }}</span>
            </div>
          </div>
          <h3 class="text-xl font-semibold text-gray-900 mb-2">{{ service.title }}</h3>
          <p class="text-gray-700">{{ service.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>