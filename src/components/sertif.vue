<script setup>
import { ref } from 'vue'

const sertifs = [
  {
    id: 1,
    name: 'Web developer',
    tahun: 'Sep 2024',
  },
  {
    id: 2,
    name: 'Programmer',
    tahun: 'Juni 2024',
  },
]

const modalOpen = ref(false)
const selectedSertif = ref(null)

function openModal(sertif) {
  selectedSertif.value = sertif
  modalOpen.value = true
}

function closeModal() {
  modalOpen.value = false
  selectedSertif.value = null
}
</script>

<template>
  <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8 text-gray-900 dark:text-slate-100">
    <div class="text-5xl font-bold text-center  my-8">Sertifikat</div>
    <div class="flex gap-8">
      <div
        v-for="sertif in sertifs"
        :key="sertif.id"
        class="group cursor-pointer  dark:border-black dark:bg-slate-800 dark:shadow-black bg-white rounded-md py-2 px-3 border border-gray-300 shadow-md "
        @click="openModal(sertif)"
      >
        <h3 class="mt-4 text-xl font-bold ">{{ sertif.name }}</h3>
        <h3 class="mt-4 text-lg font-bold ">{{ sertif.tahun }}</h3>
      </div>
    </div>

    <!-- Modal -->
    <div
      v-if="modalOpen"
      class="fixed inset-0 z-10 flex items-center justify-center bg-black bg-opacity-50"
    >
      <div class="bg-white rounded-lg p-4 shadow-lg relative max-w-lg mx-auto">
        <button
          class="absolute top-2 right-2 text-gray-400 hover:text-gray-900"
          @click="closeModal"
        >
          ✖
        </button>
        <div class="content mt-10 bg-white rounded-md ">
          <h3 class="mt-4 text-2xl font-bold text-gray-900 text-center">
            {{ selectedSertif.name }}
          </h3>
          <p class="mt-2 text-lg text-gray-600 text-center">Tahun: {{ selectedSertif.tahun }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
