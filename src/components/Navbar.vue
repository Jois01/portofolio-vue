<template>
  <nav class="bg-gray-800 sticky top-5 md:p-1 m-4 rounded-lg shadow-md">
    <div class="flex items-center justify-between">
      <div class="flex items-center">
        <a href="https://putujois.vercel.app/" class="text-xl font-bold text-emerald-500 m-4"
          >Putu Jois</a
        >
      </div>
      <div class="flex items-center text-emerald-500 text-xl font-bold">
        <a href="#Beranda" class="text-xl m-4 hidden md:block">Beranda</a>
        <a href="#about" class="text-xl m-4 hidden md:block">Tentang</a>
        <a href="#project" class="text-xl m-4 hidden md:block">Proyek</a>
        <a href="#sertif" class="text-xl m-4 hidden md:block">Sertifikat</a>
        <a href="#contact" class="text-xl m-4 hidden md:block">Kontak</a>
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
            class="size-6 stroke-emerald-600"
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
            <li class="m-3 hover:border hover:border-emerald-500 text-emerald-600 p-2 rounded-md">
              Beranda
            </li>
          </a>
          <a href="#about">
            <li class="m-3 hover:border hover:border-emerald-500 text-emerald-600 p-2 rounded-md">
              Tentang
            </li>
          </a>
          <a href="#project">
            <li class="m-3 hover:border hover:border-emerald-500 text-emerald-600 p-2 rounded-md">
              Proyek
            </li>
          </a>
          <a href="#sertif">
            <li class="m-3 hover:border hover:border-emerald-500 text-emerald-600 p-2 rounded-md">
              Sertifikat
            </li>
          </a>
          <a href="#contact">
            <li class="m-3 hover:border hover:border-emerald-500 text-emerald-600 p-2 rounded-md">
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
