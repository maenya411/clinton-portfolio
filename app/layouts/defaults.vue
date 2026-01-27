<template>
  <div class="min-h-screen flex flex-col bg-gray-50">
    <!-- Navbar -->
    <header class="bg-gray-800 text-white shadow">
      <div class="container mx-auto flex justify-between items-center p-4">
        <h1 class="text-2xl font-bold">My Portfolio</h1>
        <nav>
          <ul class="flex space-x-6">
            <li><NuxtLink to="/" class="hover:text-blue-400">Home</NuxtLink></li>
            <li><NuxtLink to="/about" class="hover:text-blue-400">About</NuxtLink></li>
            <li><NuxtLink to="/projects" class="hover:text-blue-400">Projects</NuxtLink></li>
            <li><NuxtLink to="/contact" class="hover:text-blue-400">Contact</NuxtLink></li>
          </ul>
        </nav>
      </div>
    </header>

    <!-- Page content -->
    <main class="flex-1 container mx-auto p-6">
      <slot />
    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white text-center py-6 mt-auto">
      © 2026 Clinton maenya. All rights reserved.
    </footer>
  </div>
</template>

<script setup>
</script>

<style scoped>
</style>
