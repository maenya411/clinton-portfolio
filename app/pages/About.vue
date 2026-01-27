<template>
  <div class="bg-gray-50 dark:bg-gray-900 min-h-screen">
    <Navbar />

    <!-- Hero About Section -->
    <section class="py-20 px-6 text-center bg-gradient-to-r from-blue-400 to-purple-500 text-white">
      <h1 class="text-5xl font-bold mb-4">About Me</h1>
      <p class="text-xl max-w-2xl mx-auto">
        Passionate frontend developer & creative designer
      </p>
    </section>

    <!-- Main Content -->
    <section class="py-16 px-6 max-w-5xl mx-auto flex flex-col md:flex-row items-center gap-12">
      <!-- Profile Image -->
      <div class="flex-shrink-0">
        <!-- Directly reference the image from public folder -->
        <img 
          src="/images/profile.jpg" 
          alt="Profile" 
          class="w-64 h-64 rounded-full shadow-2xl object-cover border-4 border-white dark:border-gray-700"
        />
      </div>

      <!-- About Text -->
      <div class="flex-1 space-y-6">
        <p class="text-gray-700 dark:text-gray-300 text-lg leading-relaxed">
          I am a passionate frontend developer with experience in Nuxt.js, Vue, and Tailwind CSS. I love creating beautiful, performant web applications.  
          Besides that, I also have experience in Graphic Design specializing in video editing and 3D logos using Blender, Adobe Premiere Pro, and other creative tools.
        </p>

        <!-- Skills / Expertise -->
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
          <div class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow hover:shadow-xl transition-shadow">
            <h3 class="font-bold text-lg mb-2 text-gray-900 dark:text-white">Frontend Development</h3>
            <p class="text-gray-600 dark:text-gray-300">Nuxt.js, Vue.js, Tailwind CSS, HTML, CSS, JavaScript</p>
          </div>

          <div class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow hover:shadow-xl transition-shadow">
            <h3 class="font-bold text-lg mb-2 text-gray-900 dark:text-white">Graphic Design</h3>
            <p class="text-gray-600 dark:text-gray-300">Video Editing, 3D Logos, Blender, Adobe Premiere Pro</p>
          </div>
        </div>
      </div>
    </section>

    <Footer />
  </div>
</template>

<script setup>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'


</script>
