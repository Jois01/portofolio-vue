<template>
  <nav class="bg-gray-800 sticky top-5  md:p-4 m-4 rounded-lg shadow-md">
    <div class="flex items-center justify-between">
      <div class="flex items-center text-emerald-500 text-xl font-bold">
        <!-- <img class="w-48 m-4" src="./icons/logoipsum.png" alt="" /> -->
        <div class="text-xl m-4 hidden md:block" to="#Beranda">Beranda</div>
        <div class="text-xl m-4 hidden md:block" to="#about">About</div>
      </div>

      <div id="mobile-menu" class="md:hidden flex items-center px-10">
        <div
          class="bar-menu relative inline-flex items-center justify-center rounded-md p-2 border hover:border-blue-500"
          @click="toggleMenu()"
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
              d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
            />
          </svg>
        </div>
      </div>
    </div>

    <div id="menu-dropdown" class="hidden md:hidden py-3">
      <div class="text-md ml-auto m-3">
        <div to="#Beranda">
          <div class="m-3 hover:border hover:border-blue-500 p-2 rounded-md">Beranda</div>
        </div>
        <div to="#about">
          <div class="m-3 hover:border hover:border-blue-500 p-2 rounded-md">About</div>
        </div>
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
