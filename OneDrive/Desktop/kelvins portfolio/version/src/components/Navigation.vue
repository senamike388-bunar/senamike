<template>
  <nav class="fixed top-0 w-full z-50 bg-slate-900 bg-opacity-95 backdrop-blur-sm border-b border-slate-700">
    <div class="max-w-6xl mx-auto px-4 py-4 flex justify-between items-center">
      <a href="#" class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">
        Kelvin
      </a>

      <!-- Desktop Navigation -->
      <div class="hidden md:flex space-x-8">
        <a
          href="#about"
          class="text-slate-300 hover:text-blue-400 transition-colors duration-200"
        >
          About
        </a>
        <a
          href="#experience"
          class="text-slate-300 hover:text-blue-400 transition-colors duration-200"
        >
          Experience
        </a>
        <a
          href="#projects"
          class="text-slate-300 hover:text-blue-400 transition-colors duration-200"
        >
          Projects
        </a>
        <a
          href="#contact"
          class="text-slate-300 hover:text-blue-400 transition-colors duration-200"
        >
          Contact
        </a>
      </div>

      <!-- Mobile Menu Button -->
      <button
        @click="isOpen = !isOpen"
        class="md:hidden text-slate-300 hover:text-blue-400 transition-colors"
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            :d="isOpen ? 'M6 18L18 6M6 6l12 12' : 'M4 6h16M4 12h16M4 18h16'"
          />
        </svg>
      </button>
    </div>

    <!-- Mobile Navigation -->
    <div
      v-if="isOpen"
      class="md:hidden bg-slate-800 border-t border-slate-700 px-4 py-4 space-y-3"
    >
      <a
        href="#about"
        @click="isOpen = false"
        class="block text-slate-300 hover:text-blue-400 transition-colors py-2"
      >
        About
      </a>
      <a
        href="#experience"
        @click="isOpen = false"
        class="block text-slate-300 hover:text-blue-400 transition-colors py-2"
      >
        Experience
      </a>
      <a
        href="#projects"
        @click="isOpen = false"
        class="block text-slate-300 hover:text-blue-400 transition-colors py-2"
      >
        Projects
      </a>
      <a
        href="#contact"
        @click="isOpen = false"
        class="block text-slate-300 hover:text-blue-400 transition-colors py-2"
      >
        Contact
      </a>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue';

const isOpen = ref(false);
</script>

<style scoped>
</style>
