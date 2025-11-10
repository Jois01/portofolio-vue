<script setup>
import { ref, computed } from 'vue'
import projectData from '@/store/index.json'

import IconGithub from './icons/iconGithub.vue'
import IconLihat from './icons/iconLihat.vue'
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

//data
const projects = projectData.map((project) => ({
  ...project,
  teknologi: project.teknologi.map((tech) => ({
    name: typeof tech === 'string' ? tech : tech.name,
    icon: iconMap[typeof tech === 'string' ? tech : tech.icon],
  })),
}))

// Pagination
const itemsPerPage = 6
const visibleCount = ref(itemsPerPage)

const displayedProjects = computed(() =>
  projects.slice(0, visibleCount.value)
)

const hasMoreProjects = computed(() =>
  visibleCount.value < projects.length
)

const showMoreProjects = () => {
  visibleCount.value = Math.min(visibleCount.value + 3, projects.length)
}

const showLessProjects = () => {
  visibleCount.value = itemsPerPage
}


//modal
const isModalOpen = ref(false)
const selectedProject = ref(null)

const openModal = (project) => {
  selectedProject.value = project
  isModalOpen.value = true
  document.body.classList.add('modal-open')
}

const closeModal = () => {
  isModalOpen.value = false
  selectedProject.value = null
  document.body.classList.remove('modal-open')
}

const handleBackdropClick = (e) => {
  if (e.target === e.currentTarget) closeModal()
}
</script>

<template>
  <div class="mx-auto max-w-7xl px-6 py-16">
    <!-- Title -->
    <h1 class="text-5xl font-bold text-center text-gray-900 dark:text-slate-100 my-8">Proyek</h1>

    <!-- Project Grid -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
      <div
        v-for="project in displayedProjects"
        :key="project.id"
        class="group border border-gray-300 bg-white dark:border-gray-700 dark:bg-slate-800 shadow-md rounded-lg p-4 dark:text-slate-100 hover:-translate-y-1 hover:shadow-lg transition-all duration-600"
      >
        <img :src="project.image" class="w-full rounded-lg bg-gray-200 mb-4" />
        <h3 class="text-xl font-bold mb-2">{{ project.name }}</h3>

        <!-- Tech Stack -->
        <div class="grid grid-cols-2 lg:grid-cols-3 gap-2 mb-4">
          <div
            v-for="tech in project.teknologi"
            :key="tech.name"
            class="bg-gray-900 text-gray-200 text-sm py-1 px-2 rounded-md flex items-center gap-1 border border-gray-200 shadow-sm shadow-black"
          >
            <component v-if="tech.icon" :is="tech.icon" class="size-4" />
            {{ tech.name }}
          </div>
        </div>

        <!-- Buttons -->
        <button
          @click="openModal(project)"
          class="flex items-center justify-center gap-2 w-full bg-gray-900 dark:bg-gray-900 border border-white shadow-md shadow-black hover:bg-gray-800 hover:shadow-none text-white py-2 rounded-md transition-all duration-700"
        >
          <IconLihat class="size-4" /> Detail Proyek
        </button>
      </div>
    </div>

    <!-- Show More / Less -->
  <div class="text-center mt-12">
    <button
      v-if="hasMoreProjects"
      @click="showMoreProjects"
      class="px-8 py-2 gap-2  bg-gray-900 dark:bg-gray-900 border border-white shadow-md shadow-black hover:bg-gray-800 hover:shadow-none text-white  rounded-md transition-all duration-700"
    >
      Lihat lebih banyak
    </button>

    <button
      v-else
      @click="showLessProjects"
      class="px-8 py-2 gap-2  bg-gray-900 dark:bg-gray-900 border border-white shadow-md shadow-black hover:bg-gray-800 hover:shadow-none text-white  rounded-md transition-all duration-700"
    >
      Tampilkan lebih sedikit
    </button>
  </div>

    <!-- Modal -->
    <div
      v-if="isModalOpen"
      class="fixed inset-0 bg-black/50 flex items-center justify-center p-4 z-50"
      @click="handleBackdropClick"
    >
      <div
        class="bg-white dark:bg-slate-800 rounded-lg max-w-2xl w-full overflow-y-auto max-h-[90vh] shadow-lg"
        @click.stop
      >
        <!-- Header -->
        <div
          class="flex justify-between items-center p-6 border-b border-gray-200 dark:border-gray-700"
        >
          <h3 class="text-2xl font-bold text-gray-900 dark:text-slate-100">
            {{ selectedProject?.name }}
          </h3>
          <button
            @click="closeModal"
            class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-200 p-1 rounded-full hover:bg-gray-100 dark:hover:bg-gray-700 transition"
          >
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>

        <!-- Content -->
        <div class="p-6 space-y-6">
          <img :src="selectedProject?.image" class="w-full rounded-lg bg-gray-200" />

          <section>
            <h4 class="text-lg font-semibold mb-2 dark:text-white">Deskripsi</h4>
            <p class="text-gray-700 dark:text-gray-300">
              {{ selectedProject?.description || 'Tidak ada deskripsi tersedia.' }}
            </p>
          </section>

          <section>
            <h4 class="text-lg font-semibold mb-2  dark:text-white">Teknologi</h4>
            <div class="flex flex-wrap gap-2">
              <div
                v-for="tech in selectedProject?.teknologi"
                :key="tech.name"
                class="bg-gray-900 border border-gray-200 text-sm py-1 px-2 rounded-md text-gray-200 flex items-center gap-1 shadow-sm shadow-black"
              >
                <component v-if="tech.icon" :is="tech.icon" class="size-4" />
                {{ tech.name }}
              </div>
            </div>
          </section>

          <section v-if="selectedProject?.features?.length">
            <h4 class="text-lg font-semibold mb-2">Fitur</h4>
            <ul class="list-disc pl-5 text-gray-700 dark:text-gray-300">
              <li v-for="feature in selectedProject.features" :key="feature">
                {{ feature }}
              </li>
            </ul>
          </section>

          <section class="flex gap-4 pt-4 border-t border-gray-200 dark:border-gray-700">
            <a
              v-if="selectedProject?.github"
              :href="selectedProject.github"
              target="_blank"
              rel="noopener noreferrer"
              class="flex items-center justify-center gap-2 py-2 px-4 bg-gray-900 dark:bg-gray-900 border border-white shadow-md shadow-black hover:bg-gray-800 hover:shadow-none text-white  rounded-md transition-all duration-700"
            >
              <IconGithub class="size-4" /> GitHub
            </a>
            <a
              v-if="selectedProject?.link"
              :href="selectedProject.link"
              target="_blank"
              rel="noopener noreferrer"
              class="flex items-center justify-center gap-2 py-2 px-4 bg-gray-900 dark:bg-gray-900 border border-white shadow-md shadow-black hover:bg-gray-800 hover:shadow-none text-white  rounded-md transition-all duration-700"
            >
              Lihat Website <IconLihat class="size-4" />
            </a>
          </section>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
body.modal-open {
  overflow: hidden;
}
</style>
