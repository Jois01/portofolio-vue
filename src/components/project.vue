<script setup>
import projectData from '@/store/index.json'

import iconGithub from './icons/iconGithub.vue'
import iconLihat from './icons/iconLihat.vue'
import IconHtml from './icons/iconHtml.vue'
import IconJs from './icons/iconJs.vue'
import IconLaravel from './icons/iconLaravel.vue'
import IconPHP from './icons/iconPHP.vue'
import IconTailwind from './icons/IconTailwind.vue'
import IconVue from './icons/iconVue.vue'
import IconBoostrap from './icons/iconBoostrap.vue'

const iconMap = {
  IconVue,
  IconJs,
  IconTailwind,
  IconHtml,
  IconPHP,
  IconLaravel,
  IconBoostrap,
}

const projects = projectData.map((project) => ({
  ...project,
  teknologi: project.teknologi.map((tech) => ({
    ...tech,
    icon: iconMap[tech.icon],
  })),
}))
</script>
<template>
  <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">
    <div class="text-5xl font-bold text-center text-gray-900 dark:text-slate-100 my-8">Proyek</div>
    <div
      class="grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-3 xl:gap-x-8"
    >
      <div
        v-for="project in projects"
        :key="project.id"
        class="group border border-gray-300 bg-white dark:border-black dark:bg-slate-800 dark:shadow-black shadow-md shadow-gray-300 pb-4 rounded-md p-2 dark:text-slate-100"
      >
        <img :src="project.image" class="w-full rounded-lg bg-gray-200" />
        <h3 class="mt-4 text-xl font-bold">{{ project.name }}</h3>
        <div class="mt-1 gap-2 font-medium grid lg:grid-cols-3 grid-cols-2">
          <div v-for="tech in project.teknologi" :key="tech.name">
            <div
              class="bg-gray-900 border border-gray-200 text-sm py-1 px-2 rounded-md text-gray-200 flex items-center gap-1"
            >
              <component v-if="tech.icon" :is="tech.icon" class="size-4" />

              {{ tech.name }}
            </div>
          </div>
        </div>
        <div class="flex gap-2 mt-4">
          <a
            :href="project.github"
            target="_blank"
            rel="noopener noreferrer"
            class="flex gap-2 items-center bg-gray-900 py-2 px-3 border border-gray-300 text-gray-200 rounded-md shadow-md shadow-black hover:bg-gray-800 hover:shadow-none ease-in-out duration-700"
          >
            <iconGithub class="size-4" />
            <span class="sr-only">GitHub account</span>
            Github
          </a>
          <a
            v-if="project.link"
            :href="project.link"
            target="_blank"
            rel="noopener noreferrer"
            class="flex gap-2 items-center bg-gray-900 py-2 px-3 border border-gray-300 text-gray-200 rounded-md shadow-md shadow-black hover:bg-gray-800 hover:shadow-none ease-in-out duration-700"
          >
            Website
            <span class="sr-only">Lihat Web</span>
            <iconLihat class="size-4" />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import projects from '@/store/index.json'
export default {
  data() {
    return {
      projects,
    }
  },
}
</script>
