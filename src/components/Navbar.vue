<script setup>
const navigations = [
  { name: 'Beranda', href: '#Beranda', current: true },
  { name: 'Tentang', href: '#about', current: false },
  { name: 'Proyek', href: '#project', current: false },
  { name: 'Kontak', href: '#contact', current: false },
]
</script>
<template>
  <nav class="bg-gray-800 dark:bg-slate-950 sticky top-0 pb-2 shadow-md z-50">
    <div class="flex items-center justify-between">
      <div class="flex items-center">
        <a
          href="https://putujois.vercel.app/"
          class="text-lg font-bold dark:text-slate-100 text-gray-200 m-4"
          >Putu Jois</a
        >
      </div>
      <div class="flex items-center dark:text-slate-100 text-gray-200 text-lg font-bold mx-10">
        <a
          v-for="item in navigations"
          :key="item.name"
          :href="item.href"
          class="m-4 hidden md:block"
          >{{ item.name }}</a
        >
        <div class="hidden md:block items-center">
          <label
            class="inline-flex items-center cursor-pointer border rounded-md p-1"
            :class="theme"
          >
            <input
              type="checkbox"
              value=""
              class="sr-only peer"
              v-model="toggleTheme"
              @click.prevent="toggleTheme"
            />
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="size-5"
              :class="{
                hidden: theme === 'light',
              }"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M12 3v2.25m6.364.386-1.591 1.591M21 12h-2.25m-.386 6.364-1.591-1.591M12 18.75V21m-4.773-4.227-1.591 1.591M5.25 12H3m4.227-4.773L5.636 5.636M15.75 12a3.75 3.75 0 1 1-7.5 0 3.75 3.75 0 0 1 7.5 0Z"
              />
            </svg>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="size-5"
              :class="{
                hidden: theme === 'dark',
              }"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M21.752 15.002A9.72 9.72 0 0 1 18 15.75c-5.385 0-9.75-4.365-9.75-9.75 0-1.33.266-2.597.748-3.752A9.753 9.753 0 0 0 3 11.25C3 16.635 7.365 21 12.75 21a9.753 9.753 0 0 0 9.002-5.998Z"
              />
            </svg>
          </label>
        </div>
      </div>
      <div id="mobile-menu" class="md:hidden flex items-center gap-2 text-slate-100 pr-3">
        <label class="inline-flex items-center cursor-pointer border rounded-md p-1" :class="theme">
          <input
            type="checkbox"
            value=""
            class="sr-only peer"
            v-model="toggleTheme"
            @click.prevent="toggleTheme"
          />
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="size-4"
            :class="{
              hidden: theme === 'light',
            }"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M12 3v2.25m6.364.386-1.591 1.591M21 12h-2.25m-.386 6.364-1.591-1.591M12 18.75V21m-4.773-4.227-1.591 1.591M5.25 12H3m4.227-4.773L5.636 5.636M15.75 12a3.75 3.75 0 1 1-7.5 0 3.75 3.75 0 0 1 7.5 0Z"
            />
          </svg>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="size-4"
            :class="{
              hidden: theme === 'dark',
            }"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M21.752 15.002A9.72 9.72 0 0 1 18 15.75c-5.385 0-9.75-4.365-9.75-9.75 0-1.33.266-2.597.748-3.752A9.753 9.753 0 0 0 3 11.25C3 16.635 7.365 21 12.75 21a9.753 9.753 0 0 0 9.002-5.998Z"
            />
          </svg>
        </label>
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
        <ul>
          <a v-for="item in navigations" :key="item.name" :href="item.href">
            <li
              class="m-3 hover:border hover:border-gray-200 hover:ml-6 ease-in-out duration-700 text-gray-200 p-2 rounded-md"
            >
              {{ item.name }}
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
      theme: 'light',
    }
  },
  methods: {
    toggleMenu() {
      const menuDropdown = document.getElementById('menu-dropdown')
      menuDropdown.classList.toggle('hidden')
    },
    toggleTheme() {
      this.theme = this.theme === 'light' ? 'dark' : 'light'
      this.storeThemeSetting()
      document.documentElement.classList.toggle('dark')
    },
    storeThemeSetting() {
      localStorage.setItem('theme', this.theme)
    },
    getThemeSetting() {
      let theme = localStorage.getItem('theme')
      if (theme) {
        this.theme = theme
      }
    },
  },
}
</script>
