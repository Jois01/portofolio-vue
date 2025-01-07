<template>
  <div
    class="mx-auto grid max-w-2xl grid-cols-1 text-gray-900 dark:text-slate-100 items-center gap-20 px-4 sm:px-6 sm:py-32 lg:max-w-7xl lg:grid-cols-2 lg:px-8"
    v-for="profile in profiles"
  >
    <div>
      <div class="text-3xl font-bold sm:text-5xl">
        {{ profile.salam }}
      </div>
      <div class="text-3xl font-bold sm:text-5xl my-2">{{ profile.job }}</div>
      <div class="mt-4 text-xl">
        
        <div class="mt-4 flex items-center gap-2">
          <a href="https://github.com/Jois01">
            <iconGithub
              class="size-10 hover:fill-white dark:hover:fill-white dark:fill-teal-600 ease-in-out transition-all duration-700"
            />
          </a>
          <a href="https://www.linkedin.com/in/ni-putu-jois-tika-dewi-417993253/">
            <iconLinkedin
              class="size-12 hover:fill-white dark:hover:fill-white dark:fill-teal-600 ease-in-out transition-all duration-700"
            />
          </a>
          <a href="http://putujois0703@gmail.com/">
            <iconEmail
              class="size-12 hover:stroke-white dark:hover:stroke-white dark:stroke-teal-600 ease-in-out transition-all duration-700"
            />
          </a>
        </div>
      </div>
    </div>
    <!-- Gambar Profile -->
    <div
      class="image rounded-full flex justify-center items-center sm:w-80 w-56 bg-gray-800 dark:bg-teal-800 dark:border dark:border-teal-900 mx-auto"
    >
      <div class="profile">
        <img :src="profile.image" :alt="profile.alt" class="block" />
        <div
          class="text-lg font-bold sm:w-80 w-56 bg-gray-800 dark:bg-teal-800 dark:border dark:border-teal-900 text-gray-200 text-center py-2 rounded-md"
        >
          {{ profile.name }}
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import iconGithub from './icons/iconGithub.vue'
import iconLinkedin from './icons/iconLinkedin.vue'
import iconEmail from './icons/iconEmail.vue'

const profiles = [
  {
    salam: "Hello I'm, Jois ",
    job: 'Web Development',
    name: 'Ni Putu Jois Tika Dewi',
    image: 'aku-2.png',
    alt: 'profile photo',
  },
]
</script>
