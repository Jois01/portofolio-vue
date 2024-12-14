<script setup>
import Navbar from './components/Navbar.vue'
import hero from './components/hero.vue'
import about from './components/about.vue'
import project from './components/project.vue'
import contact from './components/contact.vue'
</script>

<template>
  <Navbar />
  <section class="h-screen">
    <hero />
  </section>
  <section class="h-screen">
    <about />
  </section>
  <section>
    <project />
  </section>
  <section class="h-screen">
    <contact />
  </section>
</template>
