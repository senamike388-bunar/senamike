<template>
  <section class="py-20 px-4 bg-slate-900">
    <div class="max-w-4xl mx-auto">
      <h2 class="text-4xl md:text-5xl font-bold mb-16">
        <span class="bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">
          Work Experience
        </span>
      </h2>

      <div class="space-y-12">
        <div
          v-for="(job, index) in experiences"
          :key="index"
          class="border-l-4 border-blue-500 pl-8 py-4 hover:border-cyan-400 transition-colors duration-200"
        >
          <div class="flex flex-col md:flex-row md:items-baseline md:justify-between mb-4">
            <div>
              <h3 class="text-2xl font-bold text-slate-100 mb-2">{{ job.position }}</h3>
              <p class="text-blue-400 font-semibold">{{ job.company }}</p>
            </div>
            <p class="text-slate-400 text-sm md:text-base mt-2 md:mt-0">{{ job.period }}</p>
          </div>

          <ul class="space-y-3 mb-6 text-slate-300">
            <li v-for="(desc, i) in job.descriptions" :key="i" class="flex items-start">
              <span class="text-blue-400 mr-3 mt-1 flex-shrink-0">•</span>
              <span>{{ desc }}</span>
            </li>
          </ul>

          <div class="flex flex-wrap gap-2">
            <span
              v-for="tech in job.technologies"
              :key="tech"
              class="px-3 py-1 bg-slate-700 text-blue-300 text-sm rounded-full"
            >
              {{ tech }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const experiences = [
  {
    position: 'Full-Stack Developer',
    company: 'Tech Startup XYZ',
    period: 'Jan 2023 - Present',
    descriptions: [
      'Led development of customer-facing dashboard using Vue.js and Tailwind CSS',
      'Built scalable Node.js backend APIs handling 10,000+ daily requests',
      'Implemented real-time features using WebSockets, improving user engagement by 40%',
      'Mentored junior developers and established coding standards',
    ],
    technologies: ['Vue.js', 'Node.js', 'PostgreSQL', 'Docker', 'AWS'],
  },
  {
    position: 'Frontend Developer',
    company: 'Digital Agency ABC',
    period: 'Jun 2022 - Dec 2022',
    descriptions: [
      'Developed responsive web applications for 15+ clients using React',
      'Optimized website performance, reducing load times by 35%',
      'Collaborated with designers to implement pixel-perfect UI designs',
      'Maintained and improved legacy codebases',
    ],
    technologies: ['React', 'TypeScript', 'Tailwind CSS', 'Figma'],
  },
  {
    position: 'Freelance Web Developer',
    company: 'Self-Employed',
    period: 'Jan 2021 - May 2022',
    descriptions: [
      'Built custom websites for small businesses and startups',
      'Designed and implemented responsive web designs',
      'Provided technical support and maintenance for deployed projects',
      'Managed client relationships and project timelines',
    ],
    technologies: ['Vue.js', 'React', 'JavaScript', 'Tailwind CSS', 'MongoDB'],
  },
];
</script>

<style scoped>
</style>
