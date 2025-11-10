<script setup>
import iconGithub from './icons/iconGithub.vue'
import iconLinkedin from './icons/iconLinkedin.vue'
</script>
<template>
  <footer class="bg-gray-950">
    <div class="mx-auto w-full max-w-screen-xl p-4 py-6 lg:py-8">
      <div class="mb-6 md:flex md:justify-between">
        
        <div class="grid grid-cols-2 gap-8 sm:gap-6 sm:grid-cols-3">
          <div>
            <h2 class="mb-6 text-sm font-semibold uppercas text-white">Sumber daya</h2>
            <ul class="text-gray-400 font-medium">
              <li>
                <a href="https://tailwindcss.com/" class="hover:underline">Tailwind CSS</a>
              </li>
              <li>
                <a href="https://vuejs.org/" class="hover:underline">Vue.js</a>
              </li>
            </ul>
          </div>
          <div>
            <h2 class="mb-6 text-sm font-semibold text-white">Ikuti saya</h2>
            <ul class="text-gray-400 font-medium">
              <li class="mb-4">
                <a
                  class="hover:underline flex items-center gap-2 hover:fill-white fill-gray-500 ease-in-out transition-all duration-700"
                  href="https://github.com/Jois01"
                >
                  <iconGithub class="size-5" />
                  Github
                </a>
              </li>
              <li class="mb-4">
                <a
                  class="hover:underline flex items-center gap-2 hover:fill-white fill-gray-400 ease-in-out transition-all duration-700"
                  href="https://www.linkedin.com/in/ni-putu-jois-tika-dewi-417993253/"
                >
                  <iconLinkedin class="size-6" />
                  Linkedin
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <hr class="sm:mx-auto border-gray-700 lg:my-8" />
      <div class="text-center">
        <span class="text-sm sm:text-center text-gray-400"
          >© 2024 Jois. All Rights Reserved.
        </span>
      </div>
    </div>
  </footer>
</template>
