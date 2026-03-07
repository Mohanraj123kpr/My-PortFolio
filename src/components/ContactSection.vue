<script setup lang="ts">
import { ref } from "vue";

const form = ref({ name: "", email: "", message: "" });

function handleSubmit() {
  alert(`Thanks ${form.value.name}! Message received.`);
  form.value = { name: "", email: "", message: "" };
}
</script>

<template>
  <section id="contact" class="py-20 px-4 bg-gray-900/50">
    <div class="max-w-3xl mx-auto">
      <h2 class="text-3xl sm:text-4xl font-bold text-center mb-4">
        Get In <span class="text-cyan-400">Touch</span>
      </h2>
      <p class="text-gray-500 text-center mb-16 max-w-md mx-auto">
        Have a project in mind? Let's talk about it.
      </p>

      <form @submit.prevent="handleSubmit" class="space-y-6">
        <div class="grid sm:grid-cols-2 gap-6">
          <div>
            <label for="name" class="block text-sm text-gray-400 mb-2"
              >Name</label
            >
            <input
              id="name"
              v-model="form.name"
              type="text"
              required
              placeholder="Your name"
              class="w-full px-4 py-3 bg-gray-900 border border-gray-800 rounded-xl text-gray-200 placeholder-gray-600 focus:outline-none focus:border-cyan-500 transition-colors"
            />
          </div>
          <div>
            <label for="email" class="block text-sm text-gray-400 mb-2"
              >Email</label
            >
            <input
              id="email"
              v-model="form.email"
              type="email"
              required
              placeholder="your@email.com"
              class="w-full px-4 py-3 bg-gray-900 border border-gray-800 rounded-xl text-gray-200 placeholder-gray-600 focus:outline-none focus:border-cyan-500 transition-colors"
            />
          </div>
        </div>
        <div>
          <label for="message" class="block text-sm text-gray-400 mb-2"
            >Message</label
          >
          <textarea
            id="message"
            v-model="form.message"
            required
            rows="5"
            placeholder="Tell me about your project..."
            class="w-full px-4 py-3 bg-gray-900 border border-gray-800 rounded-xl text-gray-200 placeholder-gray-600 focus:outline-none focus:border-cyan-500 transition-colors resize-none"
          ></textarea>
        </div>
        <div class="text-center">
          <button
            type="submit"
            class="px-10 py-3 bg-gradient-to-r from-cyan-500 to-blue-600 text-white font-medium rounded-full hover:shadow-lg hover:shadow-cyan-500/25 transition-all duration-300 cursor-pointer"
          >
            Send Message
          </button>
        </div>
      </form>
    </div>
  </section>
</template>
