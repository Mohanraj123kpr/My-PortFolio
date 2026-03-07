<script setup lang="ts">
const categories = [
  {
    name: "Frameworks & Languages",
    techs: [
      "Angular",
      "Vue.js",
      "TypeScript",
      "JavaScript",
      "RxJS",
      "HTML",
      "CSS",
      "SCSS",
    ],
  },
  {
    name: "UI Libraries & Tools",
    techs: [
      "Angular Material",
      "Vuetify",
      "Tailwind CSS",
      "Bootstrap",
      "Ag-Grid",
      "Storybook",
      "PDF.js",
      "Pinia",
    ],
  },
  {
    name: "DevOps & Others",
    techs: [
      "Docker",
      "Jenkins",
      "Git",
      "MongoDB",
      "SingleSPA",
      "REST APIs",
      "WebSockets",
    ],
  },
];
</script>

<template>
  <section id="tech" class="py-20 px-4">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-3xl sm:text-4xl font-bold text-center mb-4">
        Tech <span class="text-cyan-400">Stack</span>
      </h2>
      <p class="text-gray-500 text-center mb-16 max-w-md mx-auto">
        Technologies I work with daily
      </p>

      <div class="grid md:grid-cols-3 gap-8">
        <div
          v-for="category in categories"
          :key="category.name"
          class="bg-gray-900 border border-gray-800 rounded-2xl p-6"
        >
          <h3
            class="text-sm font-semibold text-cyan-400 uppercase tracking-wider mb-5"
          >
            {{ category.name }}
          </h3>
          <div class="flex flex-wrap gap-3">
            <span
              v-for="tech in category.techs"
              :key="tech"
              class="px-4 py-2 bg-gray-800 rounded-lg text-sm text-gray-300 border border-gray-700 hover:border-cyan-500/50 transition-colors cursor-default"
            >
              {{ tech }}
            </span>
          </div>
        </div>
      </div>

      <!-- Experience bar -->
      <div
        class="mt-16 bg-gray-900 border border-gray-800 rounded-2xl p-6 sm:p-8"
      >
        <h3
          class="text-sm font-semibold text-cyan-400 uppercase tracking-wider mb-6"
        >
          Professional Experience
        </h3>
        <div class="flex flex-col sm:flex-row sm:items-center gap-4">
          <div class="flex-1">
            <p class="text-lg font-semibold text-gray-200">
              Product Engineer — Front End Developer
            </p>
            <p class="text-gray-400">Intellect Design Arena, Chennai</p>
          </div>
          <span
            class="text-sm text-gray-500 bg-gray-800 px-4 py-2 rounded-full whitespace-nowrap"
            >June 2023 — Present</span
          >
        </div>
      </div>
    </div>
  </section>
</template>
