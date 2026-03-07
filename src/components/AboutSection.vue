<template>
  <section id="about" class="py-20 px-4">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-3xl sm:text-4xl font-bold text-center mb-4">
        About <span class="text-cyan-400">Me</span>
      </h2>
      <p class="text-gray-500 text-center mb-16 max-w-md mx-auto">
        A quick glimpse into who I am
      </p>

      <div class="grid md:grid-cols-2 gap-12 items-center">
        <!-- Left: Info -->
        <div>
          <p class="text-gray-400 leading-relaxed mb-6">
            Frontend Developer with experience building dynamic, responsive, and
            high-performance web applications. Strong proficiency in Angular and
            Vue.js, with hands-on experience in component-based architecture,
            micro-frontend development, and reactive programming using RxJS.
          </p>
          <p class="text-gray-400 leading-relaxed mb-8">
            Skilled in REST API integration, UI performance optimization, and
            cross-browser compatibility. I enjoy creating reusable component
            libraries and schema-driven UI systems that scale across teams.
          </p>

          <div class="grid grid-cols-2 gap-4">
            <div
              class="bg-gray-900 border border-gray-800 rounded-xl p-4 text-center"
            >
              <p class="text-3xl font-bold text-cyan-400">3+</p>
              <p class="text-sm text-gray-500 mt-1">Years Experience</p>
            </div>
            <div
              class="bg-gray-900 border border-gray-800 rounded-xl p-4 text-center"
            >
              <p class="text-3xl font-bold text-cyan-400">3+</p>
              <p class="text-sm text-gray-500 mt-1">Production Projects</p>
            </div>
            <div
              class="bg-gray-900 border border-gray-800 rounded-xl p-4 text-center"
            >
              <p class="text-3xl font-bold text-cyan-400">B.E.</p>
              <p class="text-sm text-gray-500 mt-1">CSE, Anna University</p>
            </div>
            <div
              class="bg-gray-900 border border-gray-800 rounded-xl p-4 text-center"
            >
              <p class="text-3xl font-bold text-cyan-400">10+</p>
              <p class="text-sm text-gray-500 mt-1">Technologies</p>
            </div>
          </div>
        </div>

        <!-- Right: Details card -->
        <div class="bg-gray-900 border border-gray-800 rounded-2xl p-6 sm:p-8">
          <h3 class="text-lg font-semibold mb-6 text-gray-200">
            Personal Details
          </h3>
          <ul class="space-y-4">
            <li class="flex items-start gap-3">
              <span class="text-cyan-400 mt-0.5">
                <svg
                  class="w-5 h-5"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"
                  />
                </svg>
              </span>
              <div>
                <p class="text-xs text-gray-500 uppercase tracking-wider">
                  Name
                </p>
                <p class="text-gray-300">Mohanraj Subramanian</p>
              </div>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-cyan-400 mt-0.5">
                <svg
                  class="w-5 h-5"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                  />
                </svg>
              </span>
              <div>
                <p class="text-xs text-gray-500 uppercase tracking-wider">
                  Email
                </p>
                <p class="text-gray-300">mohanraj2002kpr@gmail.com</p>
              </div>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-cyan-400 mt-0.5">
                <svg
                  class="w-5 h-5"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
                  />
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
                  />
                </svg>
              </span>
              <div>
                <p class="text-xs text-gray-500 uppercase tracking-wider">
                  Location
                </p>
                <p class="text-gray-300">Chennai, Tamil Nadu 603103</p>
              </div>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-cyan-400 mt-0.5">
                <svg
                  class="w-5 h-5"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                  />
                </svg>
              </span>
              <div>
                <p class="text-xs text-gray-500 uppercase tracking-wider">
                  Current Role
                </p>
                <p class="text-gray-300">
                  Product Engineer at Intellect Design Arena
                </p>
              </div>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-cyan-400 mt-0.5">
                <svg
                  class="w-5 h-5"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"
                  />
                </svg>
              </span>
              <div>
                <p class="text-xs text-gray-500 uppercase tracking-wider">
                  Education
                </p>
                <p class="text-gray-300">
                  B.E. CSE — Anna University, Coimbatore (2019–2023)
                </p>
              </div>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-cyan-400 mt-0.5">
                <svg
                  class="w-5 h-5"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"
                  />
                </svg>
              </span>
              <div>
                <p class="text-xs text-gray-500 uppercase tracking-wider">
                  Availability
                </p>
                <p class="text-green-400">Open to opportunities</p>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
