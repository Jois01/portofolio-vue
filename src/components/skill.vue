<script setup>
import IconCSS from './icons/iconCSS.vue'
import IconHtml from './icons/iconHtml.vue'
import IconJs from './icons/iconJs.vue'
import IconLaravel from './icons/iconLaravel.vue'
import IconPHP from './icons/iconPHP.vue'
import IconTailwind from './icons/IconTailwind.vue'
import IconVue from './icons/iconVue.vue'
import IconBoostrap from './icons/iconBoostrap.vue'
</script>
<template>
  <div
    class="skil bg-gray-900 items-center text-center justify-center rounded-md p-8 grid grid-cols-3 gap-2"
  >
    <div>
      <IconHtml class="size-16" />
    </div>
    <div>
      <IconCSS class="size-16" />
    </div>
    <div>
      <IconTailwind class="size-16" />
    </div>
    <div>
      <IconBoostrap class="size-16" />
    </div>
    <div>
      <IconJs class="size-16" />
    </div>
    <div>
      <IconPHP class="size-16" />
    </div>
    <div>
      <IconLaravel class="size-16" />
    </div>
    <div>
      <IconVue class="size-16" />
    </div>
  </div>
</template>
