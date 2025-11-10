<template>
  <div class="container items-center mx-auto p-6 flex justify-center">
    <div
      class="border-2 border-dashed grid md:grid-cols-1 lg:grid-cols-2 items-center justify-between  border-gray-400 dark:border-gray-200 rounded-lg m-4 p-10"
    >
      <div class="md:text-left text-center items-center" v-for="contact in contacts">
        <h2 class="text-4xl font-extrabold text-gray-900 dark:text-white">{{ contact.Name }}</h2>
        <p class="mt-2 text-lg text-gray-600 dark:text-gray-400 lg:block hidden">
          {{ contact.des1 }}
        </p>
        <p class="mt-2 text-lg text-gray-600 dark:text-gray-400 lg:hidden">{{ contact.des2 }}</p>
      </div>

      <div class="mt-8 flex justify-center">
        <a
          href="mailto:putujois0703@gmail.com"
          class="py-3 px-6 text-sm md:text-lg font-semibold border border-gray-800 dark:border-white text-gray-900 dark:text-white hover:bg-gray-900 dark:hover:bg-white hover:text-white dark:hover:text-black rounded-full transition-all duration-500 ease-in-out shadow-lg flex items-center gap-2"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="size-6"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M17.25 8.25 21 12m0 0-3.75 3.75M21 12H3"
            />
          </svg>

          Tekan untuk Email
        </a>
      </div>
    </div>
  </div>
</template>
<script setup>
const contacts = [
  {
    Name: 'Hubungi Saya',
    des1: 'Punya ide keren? Atau sekadar ingin menyapa? Klik tombol di samping dan langsung kirim email ke saya. Saya tunggu kabarnya!',
    des2: ' Punya ide keren? Atau sekadar ingin menyapa? Klik tombol di bawah dan langsung kirim email ke saya. Saya tunggu kabarnya!',
  },
]
</script>
