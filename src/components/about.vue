<template>
  <div class="overflow-hidden py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="text-5xl text-gray-900 text-center font-bold mb-10">Tentang saya</div>
      <div
        class="mx-auto grid max-w-2xl grid-cols-1 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-2"
      >
        <div class="lg:pt-4 mb-8">
          <div class="lg:max-w-lg">
            <div class="text-left md:w-96">
              <h3 class="text-2xl text-gray-900 font-bold">Saya Web Developer</h3>
              <hr class="my-6 sm:mx-auto border-gray-700 lg:my-8" />
              <p class="text-gray-900 text-xl">
                Saya Ni Putu Jois Tika Dewi, mahasiswa D-3 Manajemen Informatika ITB STIKOM Bali.
                Dengan ketertarikan yang besar pada dunia web development, saya aktif terlibat dalam
                berbagai proyek semasa kuliah, seperti pengembangan web kasir dan profil perusahaan.
                Proyek-proyek ini telah membekali saya dengan keterampilan dalam HTML, CSS, dan PHP.
              </p>
            </div>
          </div>
        </div>

        <skill />
      </div>
    </div>
  </div>
</template>

<script setup>
import skill from './skill.vue'

const abouts = [
  {
    name: 'ITB Stikom Bali',
    date: 'Oktober 2022 - Sekarang',
    description: 'belum ada deskripsi.',
  },
]
</script>
