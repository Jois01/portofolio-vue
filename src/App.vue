<script setup>
import Navbar from './components/Navbar.vue'
import hero from './components/hero.vue'
import about from './components/about.vue'
import project from './components/project.vue'
import contact from './components/contact.vue'
import Footer from './components/footer.vue'
</script>

<template>
  <Navbar />
  <section id="Beranda" class="h-screen">
    <hero />
  </section>
  <section id="about" >
    <about />
  </section>
  <section id="project">
    <project />
  </section>
  <section id="contact">
    <contact />
  </section>
  <section>
    <Footer />
  </section>
</template>
