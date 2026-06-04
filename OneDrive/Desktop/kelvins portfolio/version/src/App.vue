<template>
  <div class="bg-slate-900 min-h-screen">
    <Navigation />
    <Hero />
    <section id="about" class="pt-20">
      <About />
    </section>
    <section id="experience" class="pt-20">
      <Experience />
    </section>
    <Projects />
    <Footer />
  </div>
</template>

<script setup>
import Navigation from './components/Navigation.vue';
import Hero from './components/Hero.vue';
import About from './components/About.vue';
import Experience from './components/Experience.vue';
import Projects from './components/Projects.vue';
import Footer from './components/Footer.vue';
</script>

<style scoped>
</style>
