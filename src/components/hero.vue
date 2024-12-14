<template>
  <div
    class="mx-auto grid max-w-2xl grid-cols-1 items-center gap-20 px-4 sm:px-6 sm:py-32 lg:max-w-7xl lg:grid-cols-2 lg:px-8"
    v-for="profile in profiles"
  >
    <div>
      <h2 class="text-3xl font-bold text-gray-900 sm:text-4xl">
        {{ profile.name }}
      </h2>
      <p class="mt-4 text-gray-900 text-xl">
        {{ profile.description }}
      </p>
    </div>
    <div class="image rounded-full w-80 bg-gray-800">
      <img :src="profile.image" :alt="profile.alt" class="" />
      <div class="name w-80 bg-gray-800 text-emerald-500 text-center py-2 rounded-md">
        {{ profile.name }}
      </div>
    </div>
  </div>
</template>

<script setup>
const profiles = [
  {
    name: 'Ni Putu Jois Tika Dewi',
    description:
      'TLorem ipsum dolor sit amet consectetur, adipisicing elit. Expedita maxime saepe voluptatem esse, ducimus temporibus id magni quos non molestiae?x',
    image: 'aku-2.png',
    alt: 'profile photo',
  },
]
</script>
