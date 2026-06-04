<template>
  <section class="py-20 px-4 bg-slate-800">
    <div class="max-w-4xl mx-auto">
      <div class="mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-8">
          <span class="bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">
            About Me
          </span>
        </h2>

        <div class="space-y-6 text-slate-300">
          <p class="text-lg leading-relaxed">
            I'm a passionate full-stack developer with experience in building scalable web applications and engaging user interfaces. Since starting my journey in web development, I've worked on diverse projects ranging from startups to enterprise applications.
          </p>

          <p class="text-lg leading-relaxed">
            I'm naturally curious, always learning new technologies, and dedicated to writing clean, maintainable code. I believe in creating solutions that not only work well but also provide excellent user experiences.
          </p>

          <p class="text-lg leading-relaxed">
            When I'm not coding, you can find me exploring new technologies, contributing to open-source projects, or collaborating with teams on exciting challenges.
          </p>
        </div>
      </div>

      <div>
        <h3 class="text-2xl font-bold mb-8 text-slate-100">Core Skills</h3>
        <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
          <div
            v-for="skill in skills"
            :key="skill"
            class="p-4 bg-slate-700 rounded-lg text-center hover:bg-blue-600 transition-colors duration-200 cursor-default"
          >
            <p class="text-slate-200 font-medium">{{ skill }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const skills = [
  'Vue.js',
  'React',
  'JavaScript',
  'TypeScript',
  'Tailwind CSS',
  'Node.js',
  'Express',
  'MongoDB',
  'PostgreSQL',
  'Git',
  'REST APIs',
  'Web Design',
];
</script>

<style scoped>
</style>
