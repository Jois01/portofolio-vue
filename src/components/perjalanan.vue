<template>
  <div class="max-w-7xl px-6 lg:px-8 mt-12 mx-auto items-center justify-center flex">
    <div>
      <div class="text-5xl text-center font-bold mb-10">Tempat Saya Menimba Ilmu</div>
      <ol class="relative border-s ml-4 md:ml-0 border-gray-200 dark:border-gray-700 mt-12">
        <li class="mb-10 ms-6" v-for="(about, index) in abouts" :key="index">
          <span
            class="absolute flex items-center justify-center w-6 h-6 bg-blue-100 rounded-full -start-3 ring-8 ring-white dark:ring-gray-900 dark:bg-blue-900"
          >
            <IconKalender />
          </span>
          <div
            class="items-center justify-between p-4 bg-white border border-gray-200 rounded-lg shadow-sm dark:bg-gray-700 dark:border-gray-600"
          >
            <time
              class="mb-4 sm:order-last sm:mb-0 sm:text-xl text-lg bg-gray-100 text-gray-800 font-normal me-2 px-2.5 py-0.5 rounded dark:bg-gray-600 dark:text-gray-300"
              >{{ about.date }}</time
            >
            <div class="font-normal ml-2 sm:text-lg text-md text-gray-900 dark:text-gray-300">
              {{ about.name }}
            </div>
            <div class="text-sm font-normal ml-2 text-gray-500 dark:text-gray-300 md:w-96">
              {{ about.description }}
            </div>
          </div>
        </li>
      </ol>
    </div>
  </div>
</template>

<script setup>
import IconKalender from './icons/iconKalender.vue'

const abouts = [
  {
    name: 'ITB Stikom Bali',
    date: 'Oktober 2022 - Oktober 2025',
    description:
      'Sedang menempuh pendidikan Diploma 3 dalam bidang Manajemen Informatika, fokus pada pengembangan pemrograman web, dan analisis sistem.',
  },
  {
    name: 's.p Digital',
    date: 'November 2024 - Februari 2025',
    description:
      'Mengikuti program magang sebagai Frontend Developer, berfokus pada pengembangan antarmuka pengguna menggunakan Vue.js.',
  },
]
</script>
