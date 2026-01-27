<template>
  <div class="relative">
    <Navbar />

    <!-- Contact Section -->
    <section
      class="py-20 px-6 max-w-xl mx-auto relative bg-gray-100 dark:bg-gray-800 rounded-xl shadow-lg
             transform transition duration-300 hover:scale-105 hover:shadow-2xl"
    >
      <!-- Profile Avatar Top-Left -->
      <div
        class="absolute -top-10 left-6 transform transition duration-300 hover:scale-110"
      >
        <img
          src="/images/profile.jpg"
          alt="Clinton Maenya"
          class="w-20 h-20 rounded-full border-4 border-white shadow-lg object-cover ring-2 ring-blue-400 hover:ring-purple-500 transition-all duration-300"
        />

        <!-- Name & Role below avatar -->
        <div class="mt-2 text-center">
          <p class="text-sm font-semibold text-gray-900 dark:text-white">
            Clinton Maenya
          </p>
          <p class="text-xs text-gray-500 dark:text-gray-400">Frontend Developer</p>
        </div>
      </div>

      <!-- Contact Header -->
      <h2 class="text-3xl font-bold mb-6 text-center mt-12">Contact Me</h2>

      <!-- Contact Info -->
      <div class="mb-8 grid gap-4 sm:grid-cols-2">
        <!-- Email Card -->
        <div
          class="p-6 bg-white dark:bg-gray-700 rounded-xl text-center shadow transform transition duration-300
                 hover:scale-105 hover:shadow-lg hover:bg-blue-50 dark:hover:bg-blue-900 cursor-pointer"
        >
          <p class="text-gray-700 dark:text-gray-300 mb-2 font-medium">Email Me</p>

          <!-- Hidden text appears inside card -->
          <div class="overflow-hidden">
            <p
              class="text-blue-500 dark:text-blue-400 font-semibold opacity-0 transition-opacity duration-300 hover:opacity-100"
            >
              maenyaclinton@gmail.com
            </p>
          </div>
        </div>

        <!-- WhatsApp Card -->
        <div
          class="p-6 bg-green-100 dark:bg-green-900 rounded-xl text-center shadow transform transition duration-300
                 hover:scale-105 hover:shadow-lg hover:bg-green-200 dark:hover:bg-green-800 cursor-pointer"
        >
          <p class="text-gray-800 dark:text-gray-200 mb-2 font-medium">WhatsApp Me</p>

          <!-- Hidden text appears inside card -->
          <div class="overflow-hidden">
            <p
              class="text-green-600 dark:text-green-400 font-semibold opacity-0 transition-opacity duration-300 hover:opacity-100"
            >
              +254 717 799 986
            </p>
          </div>
        </div>
      </div>

      <!-- Contact Form -->
      <form class="flex flex-col gap-4">
        <input
          type="text"
          placeholder="Name"
          class="border p-3 rounded focus:outline-none focus:ring-2 focus:ring-blue-500 transform transition duration-300 hover:scale-105"
        />
        <input
          type="email"
          placeholder="Email"
          class="border p-3 rounded focus:outline-none focus:ring-2 focus:ring-blue-500 transform transition duration-300 hover:scale-105"
        />
        <textarea
          placeholder="Message"
          class="border p-3 rounded focus:outline-none focus:ring-2 focus:ring-blue-500 transform transition duration-300 hover:scale-105"
        ></textarea>
        <button
          type="submit"
          class="bg-blue-500 text-white py-3 rounded hover:bg-blue-600 transition-colors transform transition duration-300 hover:scale-105"
        >
          Send
        </button>
      </form>
    </section>

    <Footer />
  </div>
</template>

<script setup>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'
</script>
