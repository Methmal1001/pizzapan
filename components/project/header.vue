<template>
  <header class="bg-red-600 text-white shadow-md fixed top-0 left-0 w-full z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex justify-between items-center h-16">
      <!-- Logo / Brand -->
      <div class="flex items-center">
        <span class="font-bold text-xl tracking-wider">🍕 PizzaPan</span>
      </div>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex space-x-6">
        <NuxtLink to="/" class="hover:text-yellow-300 transition">Home</NuxtLink>
        <NuxtLink to="/hr" class="hover:text-yellow-300 transition">HR</NuxtLink>
        <NuxtLink to="/sales" class="hover:text-yellow-300 transition">Sales</NuxtLink>
        <NuxtLink to="/marketing" class="hover:text-yellow-300 transition">Marketing</NuxtLink>
        <NuxtLink to="/finance" class="hover:text-yellow-300 transition">Finance</NuxtLink>
        <div>
          <NuxtLink to="/admin" class="ml-4 px-3 py-1 border border-white rounded hover:bg-white hover:text-red-600 transition">
            LogIn
          </NuxtLink>
        </div>
      </nav>

      <!-- Mobile Menu Button -->
      <button @click="toggleMenu" class="md:hidden focus:outline-none">
        <svg v-if="!isOpen" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none"
          viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none"
          viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div v-if="isOpen" class="md:hidden bg-red-500">
      <nav class="flex flex-col space-y-2 px-4 py-2">
        <NuxtLink @click="toggleMenu" to="/" class="hover:text-yellow-300 transition">Home</NuxtLink>
        <NuxtLink @click="toggleMenu" to="/hr" class="hover:text-yellow-300 transition">HR</NuxtLink>
        <NuxtLink @click="toggleMenu" to="/sales" class="hover:text-yellow-300 transition">Sales</NuxtLink>
        <NuxtLink @click="toggleMenu" to="/marketing" class="hover:text-yellow-300 transition">Marketing</NuxtLink>
        <NuxtLink @click="toggleMenu" to="/finance" class="hover:text-yellow-300 transition">Finance</NuxtLink>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
const isOpen = ref(false)

function toggleMenu() {
  isOpen.value = !isOpen.value
}
</script>

<style scoped>
/* Optional shadow for sticky header */
header {
  backdrop-filter: blur(10px);
}
</style>
