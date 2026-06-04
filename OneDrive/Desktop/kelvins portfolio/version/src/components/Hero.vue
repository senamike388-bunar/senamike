<template>
  <section class="min-h-screen flex flex-col justify-center items-center px-4 pt-20 pb-16 bg-gradient-to-b from-slate-900 to-slate-800">
    <div class="max-w-4xl mx-auto text-center">
      <div class="flex flex-col items-center lg:flex-row lg:items-start lg:justify-between gap-12 mb-12">
        <div class="max-w-2xl text-center lg:text-left">
          <h1 class="text-5xl md:text-7xl font-bold mb-4">
            <span class="bg-gradient-to-r from-blue-400 via-blue-500 to-cyan-400 bg-clip-text text-transparent">
              Hi, I'm Kelvin.
            </span>
          </h1>
          <p class="text-xl md:text-2xl text-slate-300 mb-6">
            Full-Stack Developer & Creative Problem Solver
          </p>
          <p class="text-base md:text-lg text-slate-400 max-w-2xl mx-auto lg:mx-0 mb-8">
            I build modern web applications and digital experiences. Specialized in Vue, React, and full-stack development with a passion for clean code and great UX.
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
            <a
              href="#projects"
              class="px-8 py-3 bg-blue-600 hover:bg-blue-700 text-white font-semibold rounded-lg transition-colors duration-200"
            >
              See My Work
            </a>
            <a
              href="#contact"
              class="px-8 py-3 border-2 border-blue-400 text-blue-400 hover:bg-blue-400 hover:text-slate-900 font-semibold rounded-lg transition-colors duration-200"
            >
              Get In Touch
            </a>
          </div>
        </div>

        <div class="flex-shrink-0">
          <img
            :src="profilePhoto"
            alt="Kelvin profile photo"
            class="w-48 h-48 rounded-full border-4 border-blue-500 object-cover shadow-2xl"
          />
        </div>
      </div>

      <div class="text-slate-400 text-sm">
        <p class="mb-4">BASED IN</p>
        <p class="text-lg font-semibold text-slate-200">Your Location</p>
      </div>

      <!-- Scroll indicator -->
      <div class="mt-16 animate-bounce">
        <svg class="w-6 h-6 mx-auto text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
        </svg>
      </div>
    </div>
  </section>
</template>

<script setup>
import profilePhoto from '../assets/profile.jpeg'
</script>

<style scoped>
</style>
