<script setup lang="ts">
import { ref } from "vue";

const isOpen = ref(false);

const links = [
  { label: "Home", href: "#home" },
  { label: "About", href: "#about" },
  { label: "Projects", href: "#projects" },
  { label: "Tech", href: "#tech" },
  { label: "Contact", href: "#contact" },
];

function closeMenu() {
  isOpen.value = false;
}
</script>

<template>
  <nav
    class="fixed top-0 left-0 right-0 z-50 bg-gray-950/80 backdrop-blur-md border-b border-gray-800"
  >
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <a
          href="#home"
          class="text-xl font-bold bg-gradient-to-r from-cyan-400 to-blue-500 bg-clip-text text-transparent"
        >
          Portfolio
        </a>

        <!-- Desktop links -->
        <div class="hidden md:flex items-center gap-8">
          <a
            v-for="link in links"
            :key="link.href"
            :href="link.href"
            class="text-sm text-gray-400 hover:text-cyan-400 transition-colors duration-200"
          >
            {{ link.label }}
          </a>
        </div>

        <!-- Mobile toggle -->
        <button
          class="md:hidden text-gray-400 hover:text-white"
          @click="isOpen = !isOpen"
          :aria-label="isOpen ? 'Close menu' : 'Open menu'"
          aria-expanded="false"
        >
          <svg
            class="w-6 h-6"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
          >
            <path
              v-if="!isOpen"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
            <path
              v-else
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>
    </div>

    <!-- Mobile menu -->
    <div v-if="isOpen" class="md:hidden bg-gray-900 border-t border-gray-800">
      <div class="px-4 py-3 space-y-2">
        <a
          v-for="link in links"
          :key="link.href"
          :href="link.href"
          class="block py-2 text-gray-400 hover:text-cyan-400 transition-colors"
          @click="closeMenu"
        >
          {{ link.label }}
        </a>
      </div>
    </div>
  </nav>
</template>
