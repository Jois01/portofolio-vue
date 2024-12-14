<template>
    <div class="text-5xl font-bold text-center text-gray-900 mt-4">Project</div>
    <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">
      <div
        class="grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-3 xl:gap-x-8"
      >
        <a v-for="project in projects" :key="project.id" class="group">
          <img :src="project.image" class="w-full rounded-lg bg-gray-200" />
          <h3 class="mt-4 text-lg text-gray-900">{{ project.name }}</h3>
          <div class="mt-1 text-lg gap-2 font-medium text-gray-900 grid grid-cols-3">
            <div class="items-start text-center" v-for="tech in project.teknologi" :key="tech">
              <div class="bg-gray-900 rounded-md text-emerald-600">{{ tech }}</div>
            </div>
          </div>
          <div class="flex gap-2 mt-4">
            <button
              class="bg-cyan-600 border border-gray-900 py-2 px-3 text-gray-900 rounded-md shadow-md shadow-black hover:bg-cyan-500 hover:shadow-none ease-in-out transition-all	duration-700"
            >
              Github
            </button>
            <button
              class="bg-gray-900 py-2 px-3 border border-gray-300 text-emerald-600 rounded-md shadow-md shadow-black hover:bg-gray-800 hover:shadow-none ease-in-out transition-all	duration-700"
            >
              Website
            </button>
          </div>
        </a>
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
