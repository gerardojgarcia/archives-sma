<script setup lang="ts">
import { ref } from 'vue'

const testimonials = ref([
  {
    name: 'Ana Martínez',
    title: 'Artist & Collector',
    avatar: 'https://via.placeholder.com/48',
    rating: 5,
    message:
        'Their expertise in cataloging my private collection was impeccable—every detail preserved with utmost care.'
  },
  {
    name: 'Carlos Rivera',
    title: 'Gallery Curator',
    avatar: 'https://via.placeholder.com/48',
    rating: 5,
    message:
        'We collaborated on a major exhibit; the coordination and archival documentation elevated our presentation.'
  },
  {
    name: 'María González',
    title: 'Museum Director',
    avatar: 'https://via.placeholder.com/48',
    rating: 5,
    message:
        'Their digitization services brought our historical sketches into the digital age seamlessly.'
  },
  {
    name: 'Luis Hernández',
    title: 'Archivist',
    avatar: 'https://via.placeholder.com/48',
    rating: 5,
    message:
        'Professional and thorough—condition reports were detailed and immensely helpful for preservation.'
  },
  {
    name: 'Sofía López',
    title: 'Art Dealer',
    avatar: 'https://via.placeholder.com/48',
    rating: 5,
    message:
        'Outstanding storage solutions ensured the safety of our valuable pieces during transit and storage.'
  },
  {
    name: 'Diego Torres',
    title: 'Conservator',
    avatar: 'https://via.placeholder.com/48',
    rating: 5,
    message:
        'Their conservation consulting provided practical strategies that extended the life of our collection.'
  }
])
</script>

<template>
  <section class="py-16 bg-gray-50">
    <div class="container mx-auto px-6 lg:px-8">
      <!-- Header -->
      <h2 class="text-center text-4xl font-bold mb-12">
        Client <span class="text-purple-600">Testimonials</span>
      </h2>

      <!-- Testimonials Grid -->
      <div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
        <div
            v-for="(t, i) in testimonials"
            :key="i"
            class="bg-white p-6 rounded-2xl shadow transition-shadow duration-200 hover:shadow-lg"
        >
          <!-- Star Rating -->
          <div class="flex mb-4">
            <span
                v-for="star in t.rating"
                :key="star"
                class="text-yellow-400 text-xl"
            >★</span>
          </div>

          <!-- Message -->
          <p class="text-gray-700 mb-6 leading-relaxed">
            "{{ t.message }}"
          </p>

          <hr class="border-gray-200 mb-6" />

          <!-- Client Info -->
          <div class="flex items-center">

            <div>
              <h5 class="text-lg font-semibold text-gray-900">{{ t.name }}</h5>
              <p class="text-gray-500 text-sm">{{ t.title }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>