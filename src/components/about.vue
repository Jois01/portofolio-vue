<template>
  <div class="overflow-hidden py-24 sm:py-32 text-gray-900 dark:text-slate-100">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="text-5xl text-center font-bold mb-10">Tentang saya</div>
      <div
        class="mx-auto grid max-w-2xl grid-cols-1 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-2"
      >
        <div class="lg:pt-4 mb-8 text-gray-900 dark:text-slate-100">
          <div class="lg:max-w-lg">
            <div class="text-left md:w-96">
              <h3 class="text-2xl font-bold">Saya Web Developer</h3>
              <hr class="my-6 sm:mx-auto border-gray-700 lg:my-8" />
              <p class="text-xl">
                Halo, saya Ni Putu Jois Tika Dewi, Saya berasal dari Indonesia provinsi Bali. Saya
                seorang mahasiswa D-3 Manajemen Informatika di ITB STIKOM Bali. Saya memiliki minat
                di bidang web development, saya sedang belajar menjadi Front-End Developer. Saat ini
                saya sedang belajar Vue.js dan juga Laravel
              </p>
            </div>
          </div>
        </div>

        <skill />
      </div>
    </div>
    <perjalanan />
  </div>
</template>

<script setup>
import skill from './skill.vue'
import perjalanan from './perjalanan.vue'
</script>
