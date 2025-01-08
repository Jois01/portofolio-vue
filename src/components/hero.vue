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
          <a
            href="https://github.com/Jois01"
            class="py-2 px-3 text-xs sm:text-lg border border-black dark:border-white hover:bg-slate-900 dark:hover:bg-white dark:hover:text-black rounded-full gap-2 flex items-center hover:text-white ease-in-out transition-all duration-700"
          >
            <iconGithub class="sm:size-6 size-3" />
            Github
          </a>
          <a
            href="https://www.linkedin.com/in/ni-putu-jois-tika-dewi-417993253/"
            class="py-2 px-3 text-xs sm:text-lg border border-black dark:border-white hover:bg-slate-900 dark:hover:bg-white dark:hover:text-black rounded-full gap-2 flex items-center hover:text-white ease-in-out transition-all duration-700 dark:fill-white dark:hover:fill-black hover:fill-white"
          >
            <iconLinkedin class="sm:size-7 size-4" />
            Linkedin
          </a>
          <a
            href="http://putujois0703@gmail.com/"
            class="py-2 px-3 text-xs sm:text-lg border border-black dark:border-white hover:bg-slate-900 dark:hover:bg-white dark:hover:text-black rounded-full gap-2 flex items-center hover:text-white ease-in-out transition-all duration-700"
          >
            <iconEmail class="sm:size-7 size-4" />
            Email
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
