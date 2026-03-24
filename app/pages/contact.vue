<template>
  <div class="relative">
    <Navbar />

    <!-- Contact Section -->
    <section
      class="py-20 px-6 max-w-xl mx-auto relative bg-gray-100 dark:bg-gray-800 rounded-xl shadow-lg
             transform transition duration-300 hover:scale-105 hover:shadow-2xl"
    >
      <!-- Avatar -->
      <div class="absolute -top-10 left-6 hover:scale-110 transition">
        <img
          src="/images/profile.jpg"
          alt="Clinton Maenya"
          class="w-20 h-20 rounded-full border-4 border-white shadow-lg object-cover ring-2 ring-blue-400 hover:ring-purple-500"
        />
        <div class="mt-2 text-center">
          <p class="text-sm font-semibold text-gray-900 dark:text-white">
            Clinton Maenya
          </p>
          <p class="text-xs text-gray-500 dark:text-gray-400">
            Frontend Developer
          </p>
        </div>
      </div>

      <h2 class="text-3xl font-bold mb-6 text-center mt-12">
        Contact Me
      </h2>

      <!-- Contact Cards -->
      <div class="mb-8 grid gap-4 sm:grid-cols-2">
        
        <!-- Email -->
        <div class="group p-6 bg-white dark:bg-gray-700 rounded-xl text-center shadow hover:scale-105 hover:bg-blue-50 dark:hover:bg-blue-900 cursor-pointer transition">
          <p class="text-gray-700 dark:text-gray-300 mb-2 font-medium flex items-center justify-center gap-2">
            📧 Email Me
          </p>
          <a
            href="mailto:maenyaclinton@gmail.com"
            class="text-blue-500 font-semibold opacity-0 group-hover:opacity-100 transition"
          >
            maenyaclinton@gmail.com
          </a>
        </div>

        <!-- WhatsApp -->
        <div class="group p-6 bg-green-100 dark:bg-green-900 rounded-xl text-center shadow hover:scale-105 hover:bg-green-200 dark:hover:bg-green-800 cursor-pointer transition">
          <p class="text-white mb-2 font-medium flex items-center justify-center gap-2">
            💬 WhatsApp Me
          </p>
          <a
            href="https://wa.me/254717799986"
            target="_blank"
            class="text-white font-semibold opacity-0 group-hover:opacity-100 transition"
          >
            +254 717 799 986
          </a>
        </div>
      </div>

      <!-- SUCCESS MESSAGE -->
      <p
        v-if="success"
        class="text-green-500 text-center mb-4 font-semibold animate-pulse"
      >
        ✅ Message sent successfully!
      </p>

      <!-- Contact Form -->
      <form @submit.prevent="sendEmail" class="flex flex-col gap-4">
        <input
          v-model="form.name"
          type="text"
          placeholder="Name"
          required
          class="border p-3 rounded focus:ring-2 focus:ring-blue-500"
        />
        <input
          v-model="form.email"
          type="email"
          placeholder="Email"
          required
          class="border p-3 rounded focus:ring-2 focus:ring-blue-500"
        />
        <textarea
          v-model="form.message"
          placeholder="Message"
          required
          class="border p-3 rounded focus:ring-2 focus:ring-blue-500"
        ></textarea>

        <button
          type="submit"
          class="bg-blue-500 text-white py-3 rounded hover:bg-blue-600 transition hover:scale-105"
        >
          Send Message
        </button>
      </form>
    </section>

    <Footer />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import emailjs from '@emailjs/browser'
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'

const form = ref({
  name: '',
  email: '',
  message: ''
})

const success = ref(false)

const sendEmail = () => {
  emailjs.send(
    'service_6743z8n',
    'template_jccxfsg',
    {
      from_name: form.value.name,
      from_email: form.value.email,
      message: form.value.message
    },
    'XWf5hkgh3I77F1zdt'
  )
  .then(() => {
    success.value = true
    form.value = { name: '', email: '', message: '' }

    setTimeout(() => (success.value = false), 3000)
  })
  .catch((error) => {
    console.error('FAILED...', error)
  })
}
</script>