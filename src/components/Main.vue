<template>
  <!-- PRESENTATION -->
  <section class="section-home w-100 d-flex justify-content-center align-items-center text-uppercase">
    <Home />
  </section>
  <!-- A PROPOS -->
  <section class="section-about container w-100 d-flex align-items-center">
    <About />
  </section>
  <!-- PRESENTATION -->
  <section class="section-experience container w-100 d-flex align-items-center">
    <Experience />
  </section>
  <!-- PROJECTS -->
  <section class="section-projects container w-100 d-flex align-items-center bg-primary">
    <Projects />
  </section>
</template>

<script setup>

import Home from './MainContent/Home.vue'
import About from './MainContent/About.vue'
import Experience from './MainContent/Experience.vue'
import Projects from './MainContent/Projects.vue'

</script>

<style scoped>
.section-about, .section-home {
  height: calc(100vh - 60px);
  margin: 0px !important;
}

.section-experience {
  height: 40vh;
}

.section-projects {
  height: 100vh;
}
</style>