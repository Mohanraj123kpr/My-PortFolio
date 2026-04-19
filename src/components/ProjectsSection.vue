<script setup lang="ts">
const projects = [
  {
    title: "Goal Tracker",
    description:
      "A fullstack productivity app to create, manage, and track personal goals with due dates, recurrence, and action plans. Built with a Python FastAPI backend and Angular frontend, deployed on Vercel.",
    image: "🎯",
    color: "from-cyan-500/20 to-green-500/20",
    tags: ["Angular", "Python", "FastAPI", "SQLAlchemy", "PostgreSQL", "JWT"],
    liveUrl: "https://goal-tracker-frontend-cyan.vercel.app/",
    points: [
      "Built a RESTful API with Python FastAPI covering full goal CRUD, user registration/login, and JWT-based authentication with bcrypt password hashing.",
      "Designed SQLAlchemy ORM models for users and goals with support for due dates, recurrence (daily/weekly/monthly), and action plans.",
      "Implemented Angular frontend with route guards, HTTP interceptors for token injection, and a goal dialog component for create/edit flows.",
      "Used PostgreSQL as the database with psycopg2, and structured the backend for Vercel serverless deployment via the api/ entry point.",
      "Configured CORS dynamically via environment variables to support both local development and production origins.",
    ],
  },
  {
    title: "Magic Placement",
    description:
      "Angular-based interface for insurance underwriters to extract and compare data from policy and binder documents using an LLM-powered backend.",
    image: "🏦",
    color: "from-blue-500/20 to-cyan-500/20",
    tags: [
      "Angular",
      "SCSS",
      "Angular Material",
      "PDF.js",
      "pdfjs-express",
      "RxJS",
    ],
    points: [
      "Integrated PDF rendering and annotation using PDF.js and PDF.js Express for document interaction and review workflows.",
      "Implemented RxJS-based reactive data streams for API responses, WebSocket updates, and inter-component communication — reducing redundant API calls.",
      "Created reusable services and shared components for extraction, coverage comparison, and role-based view logic.",
      "Optimized PDF rendering with lazy loading and partial rendering for large multi-page documents.",
      "Collaborated with backend teams to streamline data contracts and integrate AI-driven document extraction workflows.",
    ],
  },
  {
    title: "Risk Analyst",
    description:
      "Angular-based frontend for Intellect's data aggregation and insights platform that triangulates information from thousands of structured and unstructured data sources, providing underwriters with 360-degree intel on companies, people, and locations.",
    image: "📊",
    color: "from-emerald-500/20 to-teal-500/20",
    tags: [
      "Angular",
      "TypeScript",
      "RxJS",
      "Google Maps API",
      "SCSS",
      "Angular Material",
    ],
    points: [
      "Built interactive location intelligence views using Google Maps API, enabling underwriters to visualize risk exposure across geographies with map markers, overlays, and location-based data drill-downs.",
      "Implemented RxJS-powered reactive data pipelines to handle real-time data aggregation from multiple external and internal sources, ensuring seamless UI updates.",
      "Developed UI modules for submission data validation, enrichment workflows, and 360-degree company/people/location intel views including loss analysis dashboards.",
      "Created components for ESG insights display with custom scoring visualizations to support specialty underwriting decisions.",
      "Built Generative AI-powered summary views for accounts, policies, risks, and coverages — enabling faster triage and prioritization for underwriters.",
    ],
  },
  {
    title: "Magic Submission",
    description:
      "Vue-based AI-powered document ingestion platform for the insurance industry. Integrated with domain-trained LLMs to automate intake, contextual understanding, and processing of submission documents.",
    image: "📄",
    color: "from-purple-500/20 to-pink-500/20",
    tags: [
      "Vue 3",
      "Pinia",
      "Vuetify",
      "TypeScript",
      "SCSS",
      "Ag-Grid",
      "Storybook",
      "Jenkins",
    ],
    points: [
      "Designed a MongoDB-based configuration schema to dynamically load UI layouts, workflows, and permissions per client — enabling flexible multi-tenant rendering.",
      "Leveraged Pinia store and reactive patterns for state management, ensuring smooth sync between components and backend data streams.",
      "Integrated Ag-Grid for advanced tabular data with inline editing, filtering, and role-based visibility control.",
      "Collaborated with backend and DevOps teams for CI/CD integration through Jenkins and containerized deployment using Docker.",
    ],
  },
];

const highlights = [
  {
    icon: "🧩",
    title: "Micro-Frontend Architecture",
    description:
      "Developed and integrated microfrontend architectures using SingleSPA, enabling modular, scalable, and independently deployable front-end applications.",
  },
  {
    icon: "🎨",
    title: "Reusable Component Library",
    description:
      "Designed and developed a reusable UI component library ensuring consistency and efficiency across the application, improving development speed and maintainability.",
  },
  {
    icon: "⚙️",
    title: "Schema-Driven UI System",
    description:
      "Built a schema-based configuration system using MongoDB, allowing different clients to experience tailored UI flows through a single unified codebase.",
  },
];

const expanded = ref<string | null>(null);

function toggle(title: string) {
  expanded.value = expanded.value === title ? null : title;
}

import { ref } from "vue";
</script>

<template>
  <section id="projects" class="py-20 px-4 bg-gray-900/50">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-3xl sm:text-4xl font-bold text-center mb-4">
        My <span class="text-cyan-400">Projects</span>
      </h2>
      <p class="text-gray-500 text-center mb-16 max-w-lg mx-auto">
        Production applications built at Intellect Design Arena
      </p>

      <!-- Project cards -->
      <div class="grid md:grid-cols-3 gap-8 mb-16">
        <article
          v-for="project in projects"
          :key="project.title"
          class="group bg-gray-900 border border-gray-800 rounded-2xl overflow-hidden hover:border-cyan-500/50 transition-all duration-300"
        >
          <!-- Header -->
          <div
            :class="[
              'h-32 flex items-center justify-center text-5xl bg-gradient-to-br',
              project.color,
            ]"
          >
            {{ project.image }}
          </div>

          <div class="p-6">
            <h3 class="text-xl font-semibold text-gray-100 mb-3">
              {{ project.title }}
            </h3>
            <p class="text-sm text-gray-400 leading-relaxed mb-4">
              {{ project.description }}
            </p>

            <!-- Tags -->
            <div class="flex flex-wrap gap-2 mb-5">
              <span
                v-for="tag in project.tags"
                :key="tag"
                class="text-xs px-2.5 py-1 bg-cyan-500/10 text-cyan-400 rounded-full"
              >
                {{ tag }}
              </span>
            </div>

            <!-- Live link -->
            <a
              v-if="project.liveUrl"
              :href="project.liveUrl"
              target="_blank"
              rel="noopener"
              class="inline-flex items-center gap-1.5 text-sm text-green-400 hover:text-green-300 transition-colors mb-3"
            >
              <svg
                class="w-4 h-4"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"
                />
              </svg>
              Live Demo
            </a>

            <!-- Toggle details -->
            <button
              @click="toggle(project.title)"
              class="text-sm text-cyan-400 hover:text-cyan-300 transition-colors flex items-center gap-1.5 cursor-pointer"
            >
              <svg
                class="w-4 h-4 transition-transform duration-200"
                :class="{ 'rotate-180': expanded === project.title }"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M19 9l-7 7-7-7"
                />
              </svg>
              {{ expanded === project.title ? "Hide" : "View" }} Details
            </button>

            <!-- Expandable details -->
            <ul
              v-if="expanded === project.title"
              class="mt-4 space-y-3 border-t border-gray-800 pt-4"
            >
              <li
                v-for="(point, i) in project.points"
                :key="i"
                class="flex items-start gap-2 text-sm text-gray-400 leading-relaxed"
              >
                <span class="text-cyan-500 mt-1 shrink-0">▹</span>
                {{ point }}
              </li>
            </ul>
          </div>
        </article>
      </div>

      <!-- Key highlights -->
      <h3 class="text-xl font-semibold text-center text-gray-200 mb-8">
        Key Contributions
      </h3>
      <div class="grid sm:grid-cols-3 gap-6">
        <div
          v-for="item in highlights"
          :key="item.title"
          class="bg-gray-900 border border-gray-800 rounded-xl p-6 text-center hover:border-cyan-500/30 transition-colors"
        >
          <div class="text-3xl mb-3">{{ item.icon }}</div>
          <h4 class="text-sm font-semibold text-gray-200 mb-2">
            {{ item.title }}
          </h4>
          <p class="text-xs text-gray-500 leading-relaxed">
            {{ item.description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
