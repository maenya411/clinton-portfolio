<template>
  <footer class="bg-gradient-to-r from-gray-900 to-gray-800 text-white py-12">
    <div class="max-w-6xl mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-6">
      
      <!-- Links -->
      <ul class="flex gap-6 text-gray-300">
        <li>
          <NuxtLink to="/" class="hover:text-blue-400 transition-colors duration-300 font-semibold text-sm">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about" class="hover:text-blue-400 transition-colors duration-300 font-semibold text-sm">About</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/contact" class="hover:text-blue-400 transition-colors duration-300 font-semibold text-sm">Contact</NuxtLink>
        </li>
      </ul>
    </div>

    <!-- Bottom Copyright -->
    <div class="mt-8 text-center text-gray-400 text-xs">
      © 2026 Clinton Maenya. All rights reserved.
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
</style>
