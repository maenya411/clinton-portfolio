<template>
  <a :href="link" target="_blank" class="block">
    <div
      class="group bg-white dark:bg-gray-800 rounded-xl shadow-lg overflow-hidden border-2 border-transparent
             transform transition duration-300 hover:scale-105 hover:shadow-2xl hover:border-blue-400 hover:bg-blue-100 dark:hover:bg-blue-900 cursor-pointer"
    >
      <!-- Image with zoom on hover -->
      <img
        :src="image"
        alt="project"
        class="w-full h-48 object-cover transition-transform duration-300 group-hover:scale-110"
      />

      <!-- Project Info -->
      <div class="p-6">
        <h3
          class="text-xl font-semibold mb-2 text-gray-900 dark:text-white transition-colors duration-300 group-hover:text-blue-600"
        >
          {{ title }}
        </h3>
        <p class="text-gray-700 dark:text-gray-300 mb-4 group-hover:text-blue-700 dark:group-hover:text-blue-300 transition-colors duration-300">
          {{ description }}
        </p>
        <a
          :href="link"
          target="_blank"
          class="inline-block bg-blue-500 text-white px-4 py-2 rounded-lg group-hover:bg-blue-600 transition-colors"
        >
          View Project.
        </a>
      </div>
    </div>
  </a>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  image: String,
  link: String,
})
</script>
