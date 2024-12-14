<template>
  <div id="about">
    <div class="text-5xl text-center font-bold text-gray-900 my-8">Tentang saya</div>
    <div class="mx-auto mt-10 max-w-2xl items-center justify-center px-4 my-10">
      <ol class="relative border-s border-gray-200 dark:border-gray-700" v-for="about in abouts">
        <li class="mb-1 ms-4">
          <div
            class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -start-1.5 border border-white dark:border-gray-900 dark:bg-gray-700"
          ></div>
          <time class="mb-1 text-sm font-normal leading-none text-gray-400 dark:text-gray-500"
            >{{ about.date }}</time
          >
          <h3 class="text-lg font-semibold text-gray-900 dark:text-white">
            {{ about.name }}
          </h3>
          <p class="text-base font-normal text-gray-500 dark:text-gray-400">
           {{about.description}}
          </p>
        </li>
      </ol>
    </div>
  </div>
</template>

<script setup>
const abouts = [
  {
    name: 'ITB Stikom Bali',
    date: 'Oktober 2022 - Sekarang',
    description:
      'belum ada deskripsi.',
  },
  {
    name: 'ITB Stikom Bali',
    date: 'Oktober 2022 - Sekarang',
    description:
      'belum ada deskripsi.',
  },
]
</script>
