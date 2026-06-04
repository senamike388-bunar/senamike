<template>
  <section id="projects" class="py-20 px-4 bg-slate-800">
    <div class="max-w-5xl mx-auto">
      <h2 class="text-4xl md:text-5xl font-bold mb-16">
        <span class="bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">
          Notable Projects
        </span>
      </h2>

      <div class="grid md:grid-cols-2 gap-8">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="group bg-slate-700 rounded-lg overflow-hidden hover:shadow-xl transition-all duration-300 hover:shadow-blue-500/50"
        >
          <!-- Project Image -->
          <div class="h-48 bg-gradient-to-br from-blue-600 to-cyan-500 overflow-hidden relative">
            <div class="w-full h-full flex items-center justify-center text-slate-100 text-6xl opacity-30">
              {{ project.icon }}
            </div>
            <div class="absolute inset-0 bg-black opacity-0 group-hover:opacity-40 transition-opacity duration-300" />
          </div>

          <!-- Project Content -->
          <div class="p-6">
            <h3 class="text-xl font-bold text-slate-100 mb-2">{{ project.name }}</h3>
            <p class="text-slate-300 mb-4 text-sm leading-relaxed">{{ project.description }}</p>

            <!-- Technologies -->
            <div class="mb-6 flex flex-wrap gap-2">
              <span
                v-for="tech in project.technologies"
                :key="tech"
                class="px-2 py-1 bg-slate-600 text-blue-300 text-xs rounded"
              >
                {{ tech }}
              </span>
            </div>

            <!-- Links -->
            <div class="flex gap-4">
              <a
                v-if="project.github"
                :href="project.github"
                target="_blank"
                class="inline-flex items-center text-blue-400 hover:text-blue-300 font-medium text-sm transition-colors"
              >
                <svg class="w-4 h-4 mr-2" fill="currentColor" viewBox="0 0 24 24">
                  <path
                    d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 . 405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.001 12.001 0 0024 12c0-6.63-5.37-12-12-12z"
                  />
                </svg>
                GitHub
              </a>
              <a
                v-if="project.link"
                :href="project.link"
                target="_blank"
                class="inline-flex items-center text-blue-400 hover:text-blue-300 font-medium text-sm transition-colors"
              >
                <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4m-4-6l6-6m0 0l-6 6m6-6v6"
                  />
                </svg>
                Live Demo
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    name: 'E-Commerce Platform',
    icon: '🛒',
    description:
      'A full-stack e-commerce application with product catalog, shopping cart, user authentication, and payment integration. Built with Vue.js frontend and Node.js backend.',
    technologies: ['Vue.js', 'Node.js', 'MongoDB', 'Stripe', 'JWT'],
    github: 'https://github.com',
    link: '#',
  },
  {
    name: 'Task Management App',
    icon: '✓',
    description:
      'Real-time collaborative task management application with drag-and-drop functionality, team collaboration features, and notifications. Uses Firebase for real-time updates.',
    technologies: ['React', 'Firebase', 'Tailwind CSS', 'Redux'],
    github: 'https://github.com',
    link: '#',
  },
  {
    name: 'Social Media Analytics',
    icon: '📊',
    description:
      'Dashboard for analyzing social media metrics with interactive charts and real-time data visualization. Integrates with multiple social media APIs.',
    technologies: ['Vue.js', 'Chart.js', 'Node.js', 'PostgreSQL', 'Docker'],
    github: 'https://github.com',
    link: '#',
  },
  {
    name: 'Weather Forecast App',
    icon: '🌤️',
    description:
      'Progressive Web App for real-time weather forecasting with location-based services, maps integration, and offline functionality for better user experience.',
    technologies: ['React', 'OpenWeather API', 'PWA', 'Mapbox', 'Service Workers'],
    github: 'https://github.com',
    link: '#',
  },
];
</script>

<style scoped>
</style>
