<template>
  <div class="container items-center mx-auto">
    <form>
      <div class="m-10 gap-x-6 gap-y-8">
        <div class="text-5xl font-bold text-center text-gray-900 my-8">Contact Me</div>
        <div class="mt-10 grid grid-cols-2 gap-x-6 gap-y-8">
          <div class="my-4">
            <label for="nama" class="block text-sm/6 font-medium text-gray-900"> Your name</label>
            <div class="mt-2">
              <div
                class="flex items-center rounded-md bg-white px-3 py-1.5 text-base text-gray-900 outline outline-1 -outline-offset-1 outline-gray-300 focus-within:outline focus-within:outline-2 focus-within:-outline-offset-2 focus-within:outline-indigo-600"
              >
                <input
                
                  type="text"
                  name="nama"
                  id="nama"
                  class="block min-w-0 grow py-1.5 pl-1 pr-3 text-base text-gray-900 placeholder:text-gray-400 focus:outline focus:outline-0 sm:text-sm/6"
                  placeholder="Your name"
                />
              </div>
            </div>
          </div>
          <div class="my-4">
            <label for="email" class="block text-sm/6 font-medium text-gray-900">Email</label>
            <div class="mt-2">
              <div
                class="flex items-center rounded-md bg-white px-3 py-1.5 text-base text-gray-900 outline outline-1 -outline-offset-1 outline-gray-300 focus-within:outline focus-within:outline-2 focus-within:-outline-offset-2 focus-within:outline-indigo-600"
              >
                <input
                  type="email"
                  name="email"
                  id="email"
                  class="block min-w-0 grow py-1.5 pl-1 pr-3 text-base text-gray-900 placeholder:text-gray-400 focus:outline focus:outline-0 sm:text-sm/6"
                  placeholder="email@gmail.com"
                />
              </div>
            </div>
          </div>
        </div>

        <div class="col-span-full">
          <label for="about" class="block text-sm/6 font-medium text-gray-900">Deskripsi</label>
          <div class="mt-2">
            <textarea
              name="about"
              id="about"
              rows="3"
              class="block w-full rounded-md bg-white px-3 py-1.5 text-base text-gray-900 outline outline-1 -outline-offset-1 outline-gray-300 placeholder:text-gray-400 focus:outline focus:outline-2 focus:-outline-offset-2 focus:outline-indigo-600 sm:text-sm/6"
            />
          </div>
        </div>

        <div class="flex items-center justify-end gap-x-6 mt-4">
          <button
            type="button"
            class="text-sm/6 bg-red-600 border py-2 px-3 border-gray-900 font-semibold text-white rounded-md shadow-md shadow-black hover:bg-red-500 hover:shadow-none ease-in-out transition-all duration-700"
          >
            Cancel
          </button>

          <button
            type="submit"
            class="bg-cyan-600 border border-gray-900 py-2 px-3 text-white rounded-md shadow-md shadow-black hover:bg-cyan-500 hover:shadow-none ease-in-out transition-all duration-700"
          >
            Save
          </button>
        </div>
      </div>
    </form>
  </div>
</template>
