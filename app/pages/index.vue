<template>
  <div class="bg-gray-50 dark:bg-gray-900 min-h-screen">
    <!-- Navbar -->
    <Navbar />

    <!-- Hero Section -->
    <section
      class="text-center py-24 bg-gradient-to-r from-blue-400 to-purple-500 text-white relative"
    >
      <!-- Floating decor circle -->
      <div
        class="absolute top-0 left-1/2 transform -translate-x-1/2 mt-4 w-24 h-24 bg-white/10 rounded-full animate-pulse"
      ></div>

      <!-- Typing Text -->
      <h1 class="text-5xl font-bold mb-4">
        {{ displayedText }}
        <span v-if="isTyping" class="animate-pulse">|</span>
      </h1>

      <p class="text-xl mb-6">
        Full Software Developer | Nuxt.js & Tailwind CSS | Graphic Designer
      </p>

      <!-- Profile Avatar -->
      <div class="inline-block relative">
        <img
          src="/images/profile.jpg"
          alt="Clinton Maenya"
          class="w-24 h-24 rounded-full object-cover border-4 border-white shadow-xl ring-2 ring-blue-300 hover:ring-purple-400 transition-all duration-300 cursor-pointer"
        />

        <!-- Online status -->
        <span
          class="absolute bottom-1 right-1 w-4 h-4 bg-green-400 border-2 border-white rounded-full"
        ></span>
      </div>

      <!-- Name & Role -->
      <div class="mt-4">
        <p class="text-xl font-semibold">
          Here we create solutions for everything concerning tech world
        </p>
        <p class="text-sm text-white/80">
          Frontend Developer & Graphic Designer
        </p>
      </div>
    </section>

    <!-- Projects Section -->
    <section class="py-20 px-6 bg-gray-100 dark:bg-gray-800">
      <h2
        class="text-3xl font-bold text-center text-gray-900 dark:text-white mb-12"
      >
        My Projects
      </h2>

      <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
        <ProjectCard
          v-for="(project, index) in projects"
          :key="index"
          :title="project.title"
          :description="project.description"
          :image="project.image"
          :link="project.link"
        />
      </div>
    </section>

    <!-- Footer -->
    <Footer />
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'
import ProjectCard from '~/components/projects/ProjectCard.vue'

// Typing effect state
const fullText = "Hi, I'm Clinton Maenya"
const displayedText = ref('')
const isTyping = ref(true)
const typingSpeed = 100

onMounted(() => {
  let index = 0
  const interval = setInterval(() => {
    if (index < fullText.length) {
      displayedText.value += fullText[index]
      index++
    } else {
      isTyping.value = false // hide cursor after typing finishes
      clearInterval(interval)
    }
  }, typingSpeed)
})

// Projects data
const projects = [
  {
    title: 'Portfolio Website',
    description: 'A sleek portfolio built with Nuxt 3 & Tailwind CSS.',
    image: '/images/project1.jpg',
    link: '#'
  },
  {
    title: 'E-commerce App',
    description: 'A full-featured e-commerce platform.',
    image: '/images/project2.jpg',
    link: '#'
  },
  {
    title: 'Blog Platform',
    description: 'A modern blogging platform with Markdown support.',
    image: '/images/project4.jpeg',
    link: '#'
  }
]
</script>
