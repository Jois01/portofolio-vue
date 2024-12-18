<script setup>
import Navbar from './components/Navbar.vue'
import hero from './components/hero.vue'
import about from './components/about.vue'
import project from './components/project.vue'
import sertif from './components/sertif.vue'
import contact from './components/contact.vue'
import Footer from './components/footer.vue'
</script>

<template>
  <Navbar />
  <section id="Beranda" >
    <hero />
  </section>
  <section id="about" >
    <about />
  </section>
  <section id="project">
    <project />
  </section>
  <section id="sertif">
    <sertif />
  </section>
  <section id="contact">
    <contact />
  </section>
  <section>
    <Footer />
  </section>
</template>
