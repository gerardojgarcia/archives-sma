<script setup lang="ts">

</script>

<template>
  <section class="relative py-20">
    <!-- Background Image -->
    <img
        src="/kelly-studio.png"
        alt="Ellsworth Kelly Inspired Background"
        class="absolute inset-0 w-full h-full object-cover opacity-20"
    />

    <div class="relative container mx-auto px-6 lg:px-8">
      <h2 class="text-center text-4xl lg:text-5xl font-bold mb-16">
        <span class="text-purple-600">Our Archival</span> Case Studies
      </h2>

      <div class="max-w-3xl mx-auto">
        <!-- Single case card -->
        <div class="bg-white p-8 rounded-3xl shadow-lg relative">
          <!-- Tags -->
          <div class="flex space-x-3 mb-4">
            <span class="px-3 py-1 border border-gray-300 rounded-full text-sm text-gray-700">
              Provenance
            </span>
            <span class="px-3 py-1 border border-gray-300 rounded-full text-sm text-gray-700">
              Digitization
            </span>
          </div>

          <h3 class="text-2xl font-semibold text-gray-900 mb-4">
            Cataloging a Maestro’s Sketch Collection
          </h3>

          <p class="text-gray-700 mb-6">
            Detailed inventory and digital conversion of a prominent artist’s preliminary drawings,
            ensuring preservation of metadata and historical context.
          </p>

          <button class="inline-flex items-center justify-center w-12 h-12 bg-black text-white rounded-full hover:bg-gray-800 transition">
            <span class="text-2xl">+</span>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>