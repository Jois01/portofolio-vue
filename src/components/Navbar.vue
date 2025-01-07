<template>
  <nav class="bg-gray-800 sticky top-5 md:p-1 m-4 rounded-lg shadow-md">
    <div class="flex items-center justify-between">
      <div class="flex items-center">
        <a href="https://putujois.vercel.app/" class="text-xl font-bold text-gray-200 m-4"
          >Putu Jois</a
        >
      </div>
      <div class="flex items-center text-gray-200 text-xl font-bold mr-7">
        <a href="#Beranda" class="text-xl m-4 hidden md:block">Beranda</a>
        <a href="#about" class="text-xl m-4 hidden md:block">Tentang</a>
        <a href="#project" class="text-xl m-4 hidden md:block">Proyek</a>
        <a href="#sertif" class="text-xl m-4 hidden md:block">Sertifikat</a>
        <a href="#contact" class="text-xl m-4 hidden md:block">Kontak</a>
        <button class="text-xl m-4 hidden md:block">
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
              d="M12 3v2.25m6.364.386-1.591 1.591M21 12h-2.25m-.386 6.364-1.591-1.591M12 18.75V21m-4.773-4.227-1.591 1.591M5.25 12H3m4.227-4.773L5.636 5.636M15.75 12a3.75 3.75 0 1 1-7.5 0 3.75 3.75 0 0 1 7.5 0Z"
            />
          </svg>
        </button>
      </div>

      <div id="mobile-menu" class="md:hidden flex items-center px-10">
        <div
          class="bar-menu relative inline-flex items-center justify-center rounded-md p-2"
          @click="toggleMenu()"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="size-6 stroke-gray-200"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
            />
          </svg>
        </div>
      </div>
    </div>

    <div id="menu-dropdown" class="hidden md:hidden py-3">
      <div class="text-md ml-auto m-3">
        <ul>
          <a href="#Beranda">
            <li
              class="m-3 hover:border hover:border-gray-200 hover:ml-6 ease-in-out duration-700 text-gray-200 p-2 rounded-md"
            >
              Beranda
            </li>
          </a>
          <a href="#about">
            <li
              class="m-3 hover:border hover:border-gray-200 hover:ml-6 ease-in-out duration-700 text-gray-200 p-2 rounded-md"
            >
              Tentang
            </li>
          </a>
          <a href="#project">
            <li
              class="m-3 hover:border hover:border-gray-200 hover:ml-6 ease-in-out duration-700 text-gray-200 p-2 rounded-md"
            >
              Proyek
            </li>
          </a>
          <a href="#sertif">
            <li
              class="m-3 hover:border hover:border-gray-200 hover:ml-6 ease-in-out duration-700 text-gray-200 p-2 rounded-md"
            >
              Sertifikat
            </li>
          </a>
          <a href="#contact">
            <li
              class="m-3 hover:border hover:border-gray-200 hover:ml-6 ease-in-out duration-700 text-gray-200 p-2 rounded-md"
            >
              Kontak
            </li>
          </a>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      Open: false,
    }
  },
  methods: {
    toggleMenu() {
      const menuDropdown = document.getElementById('menu-dropdown')
      menuDropdown.classList.toggle('hidden')
    },
  },
}
</script>
