<script setup>
import IconCSS from './icons/iconCSS.vue'
import IconHtml from './icons/iconHtml.vue'
import IconJs from './icons/iconJs.vue'
import IconLaravel from './icons/iconLaravel.vue'
import IconPHP from './icons/iconPHP.vue'
import IconTailwind from './icons/IconTailwind.vue'
import IconVue from './icons/iconVue.vue'
import IconBoostrap from './icons/iconBoostrap.vue'

const skills = [
  { component: IconHtml, name: 'HTML' },
  { component: IconCSS, name: 'CSS' },
  { component: IconTailwind, name: 'Tailwind' },
  { component: IconBoostrap, name: 'Bootstrap' },
  { component: IconJs, name: 'JavaScript' },
  { component: IconPHP, name: 'PHP' },
  { component: IconLaravel, name: 'Laravel' },
  { component: IconVue, name: 'Vue.js' },
]
</script>

<template>
  <div class="skil bg-gray-900 items-center text-center justify-center rounded-md p-8 grid grid-cols-3 gap-4">
    <!-- Loop through the skills array -->
    <div
      v-for="(skill, index) in skills"
      :key="index"
      class="flex flex-col items-center justify-center text-gray-900 rounded-md hover:shadow-md hover:shadow-black py-4 px-3 ease-in-out duration-700"
    >
      <!-- Render the icon component dynamically -->
      <component :is="skill.component" class="size-16 mb-2" />
      <p class="text-gray-400 text-sm">{{ skill.name }}</p>
    </div>
  </div>
</template>
