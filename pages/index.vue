<template>
  <div class="my-5 bg-gray-700 p-8">
    <h1 class="text-4xl font-extrabold mb-10 text-yellow-400 text-center">🍕 Pizza Shop Dashboard</h1>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-5 gap-6">
      <div
        class="bg-gradient-to-br from-red-700 to-yellow-500 p-6 rounded-2xl shadow-2xl 
                transform hover:scale-105 hover:shadow-xl transition-all flex items-center justify-center gap-3 cursor-pointer"
        @click="navigate('hr')"
        >
        <!-- SVG Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M5.121 17.804A8.003 8.003 0 0112 15c1.657 0 3.156.507 4.379 1.372M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
        </svg>

        <!-- Text -->
        <span class="text-xl font-bold text-white">HR Portal</span>
    </div>

      <!-- Sales Portal -->
    <div
    class="bg-gradient-to-br from-red-700 to-yellow-500 p-6 rounded-2xl shadow-2xl 
            transform hover:scale-105 hover:shadow-xl transition-all flex items-center justify-center gap-3 cursor-pointer"
    @click="navigate('sales')"
    >
    <!-- SVG Icon for Sales -->
    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M3 3v18h18M3 9h18M3 15h18" />
    </svg>
    <span class="text-xl font-bold text-white">Sales Portal</span>
    </div>

    <!-- Marketing Portal -->
    <div
    class="bg-gradient-to-br from-red-700 to-yellow-500 p-6 rounded-2xl shadow-2xl 
            transform hover:scale-105 hover:shadow-xl transition-all flex items-center justify-center gap-3 cursor-pointer"
    @click="navigate('marketing')"
    >
    <!-- SVG Icon for Marketing -->
    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M8 12h8m-8 4h8M4 6h16M4 18h16" />
    </svg>
    <span class="text-xl font-bold text-white">Marketing</span>
    </div>

    <!-- Billing Portal -->
    <div
    class="bg-gradient-to-br from-red-700 to-yellow-500 p-6 rounded-2xl shadow-2xl 
            transform hover:scale-105 hover:shadow-xl transition-all flex items-center justify-center gap-3 cursor-pointer"
    @click="navigate('billing')"
    >
    <!-- SVG Icon for Billing -->
    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2" />
    </svg>
    <span class="text-xl font-bold text-white">Billing Portal</span>
    </div>

    <!-- Finance Portal -->
    <div
    class="bg-gradient-to-br from-red-700 to-yellow-500 p-6 rounded-2xl shadow-2xl 
            transform hover:scale-105 hover:shadow-xl transition-all flex items-center justify-center gap-3 cursor-pointer"
    @click="navigate('finance')"
    >
    <!-- SVG Icon for Finance -->
    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M12 8v8m4-4H8" />
    </svg>
    <span class="text-xl font-bold text-white">Finance</span>
    </div>

    </div>
  </div>
</template>

<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()

const navigate = (page) => {
  router.push(`/${page}`)
}
</script>

<style>
/* Optional: add a subtle animated background glow */
body {
  background-image: radial-gradient(circle at top left, rgba(255, 200, 0, 0.1), rgba(0,0,0,0.9));
}
</style>
