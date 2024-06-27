<template>
  <div>
    <header class="bg-gray-800 text-white py-4">
      <div class="container mx-auto px-4">
        <div class="flex items-center justify-between">
          <div class="text-lg font-bold">My Website</div>
          <button @click="toggleMenu" class="md:hidden focus:outline-none">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6 text-white"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16m-7 6h7"
              />
            </svg>
          </button>
          <nav class="hidden md:block">
            <ul class="flex space-x-4">
              <li>
                <a
                  href="/"
                  class="block px-3 py-2 rounded-md text-sm font-medium text-white hover:bg-gray-700"
                  >Home</a
                >
              </li>
              <li>
                <a
                  href="/about"
                  class="block px-3 py-2 rounded-md text-sm font-medium text-white hover:bg-gray-700"
                  >About</a
                >
              </li>
              <li>
                <a
                  href="/contact"
                  class="block px-3 py-2 rounded-md text-sm font-medium text-white hover:bg-gray-700"
                  >Contact</a
                >
              </li>
            </ul>
          </nav>
        </div>
        <nav
          :class="{ block: menuOpen, hidden: !menuOpen }"
          class="md:hidden mt-4"
        >
          <ul>
            <li>
              <a
                href="/"
                class="block px-3 py-2 rounded-md text-sm font-medium text-white hover:bg-gray-700"
                >Home</a
              >
            </li>
            <li>
              <a
                href="/about"
                class="block px-3 py-2 rounded-md text-sm font-medium text-white hover:bg-gray-700"
                >About</a
              >
            </li>
            <li>
              <a
                href="/contact"
                class="block px-3 py-2 rounded-md text-sm font-medium text-white hover:bg-gray-700"
                >Contact</a
              >
            </li>
          </ul>
        </nav>
      </div>
    </header>
  </div>
</template>

<script setup>
import { Head } from "@inertiajs/vue3";
import { ref } from "vue";

const menuOpen = ref(false);

function toggleMenu() {
  menuOpen.value = !menuOpen.value;
}
</script>