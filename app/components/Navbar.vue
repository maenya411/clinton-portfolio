<template>
  <nav class="flex justify-between items-center p-6 bg-gray-800 text-white shadow-lg">
    <!-- Stylish Box for Name -->
    <div
      class="bg-gradient-to-r from-blue-500 to-purple-500 px-4 py-2 rounded-lg shadow-md font-bold text-white text-lg 
             hover:scale-105 hover:shadow-xl hover:from-purple-500 hover:to-pink-500 transform transition-all duration-300 cursor-pointer"
    >
      @Clinton Maenya
    </div>

    <!-- Nav Links -->
    <ul class="flex gap-6">
      <li>
        <NuxtLink
          to="/"
          class="relative group text-white font-medium transition-colors duration-300 hover:text-blue-400"
        >
          Home
          <!-- Underline effect -->
          <span
            class="absolute left-0 -bottom-1 w-0 h-0.5 bg-blue-400 transition-all duration-300 group-hover:w-full"
          ></span>
        </NuxtLink>
      </li>
      <li>
        <NuxtLink
          to="/about"
          class="relative group text-white font-medium transition-colors duration-300 hover:text-blue-400"
        >
          About
          <span
            class="absolute left-0 -bottom-1 w-0 h-0.5 bg-blue-400 transition-all duration-300 group-hover:w-full"
          ></span>
        </NuxtLink>
      </li>
      <li>
        <NuxtLink
          to="/contact"
          class="relative group text-white font-medium transition-colors duration-300 hover:text-blue-400"
        >
          Contact
          <span
            class="absolute left-0 -bottom-1 w-0 h-0.5 bg-blue-400 transition-all duration-300 group-hover:w-full"
          ></span>
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script setup>
</script>

<style scoped>
</style>
