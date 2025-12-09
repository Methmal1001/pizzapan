<template>
  <footer class="bg-gradient-to-r from-red-600 to-red-700 text-white mt-12">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12 grid grid-cols-1 md:grid-cols-3 gap-8">

      <!-- Brand & Description -->
      <div class="space-y-4">
        <span class="font-bold text-2xl tracking-wider flex items-center gap-2">
          <span class="text-yellow-400 text-3xl">🍕</span> PizzaPan
        </span>
        <p class="text-gray-200">
          All-in-one management for your pizza business: HR, Sales, Marketing, Finance, and more.
        </p>
      </div>

      <!-- Quick Links -->
      <div>
        <h3 class="font-semibold text-lg mb-4">Quick Links</h3>
        <ul class="space-y-2">
          <li>
            <NuxtLink to="/" class="hover:text-yellow-400 transition duration-300">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/hr" class="hover:text-yellow-400 transition duration-300">HR</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/sales" class="hover:text-yellow-400 transition duration-300">Sales</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/marketing" class="hover:text-yellow-400 transition duration-300">Marketing</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/finance" class="hover:text-yellow-400 transition duration-300">Finance</NuxtLink>
          </li>
        </ul>
      </div>

      <!-- Contact / Social -->
      <div class="space-y-4">
        <h3 class="font-semibold text-lg mb-2">Contact Us</h3>
        <p class="text-gray-200">support@pizzapan.com</p>
        <div class="flex space-x-4">
          <!-- Twitter -->
          <a href="#" class="p-2 rounded-full bg-red-500 hover:bg-yellow-400 hover:text-red-700 transition duration-300">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
              <path d="M24 4.557a9.83 9.83 0 01-2.828.775 4.932 4.932 0 002.165-2.724 9.864 9.864 0 01-3.127 1.195 4.916 4.916 0 00-8.38 4.482A13.939 13.939 0 011.671 3.149a4.916 4.916 0 001.523 6.574 4.903 4.903 0 01-2.229-.616c-.054 2.28 1.581 4.415 3.949 4.89a4.936 4.936 0 01-2.224.084 4.919 4.919 0 004.59 3.417 9.867 9.867 0 01-6.102 2.104c-.396 0-.788-.023-1.175-.069a13.945 13.945 0 007.548 2.212c9.057 0 14.009-7.513 14.009-14.009 0-.213-.005-.425-.014-.636A10.012 10.012 0 0024 4.557z"/>
            </svg>
          </a>

          <!-- Instagram -->
          <a href="#" class="p-2 rounded-full bg-red-500 hover:bg-yellow-400 hover:text-red-700 transition duration-300">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 2.163c3.204 0 3.584.012 4.85.07 1.366.062 2.633.342 3.608 1.317.975.975 1.255 2.242 1.317 3.608.058 1.266.07 1.646.07 4.85s-.012 3.584-.07 4.85c-.062 1.366-.342 2.633-1.317 3.608-.975.975-2.242 1.255-3.608 1.317-1.266.058-1.646.07-4.85.07s-3.584-.012-4.85-.07c-1.366-.062-2.633-.342-3.608-1.317-.975-.975-1.255-2.242-1.317-3.608-.058-1.266-.07-1.646-.07-4.85s.012-3.584.07-4.85c.062-1.366.342-2.633 1.317-3.608.975-.975 2.242-1.255 3.608-1.317 1.266-.058 1.646-.07 4.85-.07M12 0C8.741 0 8.332.013 7.052.072 5.775.131 4.603.433 3.678 1.358 2.753 2.283 2.451 3.455 2.392 4.732 2.333 6.012 2.32 6.421 2.32 9.68s.013 3.668.072 4.948c.059 1.277.361 2.449 1.286 3.374.925.925 2.097 1.227 3.374 1.286 1.28.059 1.689.072 4.948.072s3.668-.013 4.948-.072c1.277-.059 2.449-.361 3.374-1.286.925-.925 1.227-2.097 1.286-3.374.059-1.28.072-1.689.072-4.948s-.013-3.668-.072-4.948c-.059-1.277-.361-2.449-1.286-3.374-.925-.925-2.097-1.227-3.374-1.286C15.668.013 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zm0 10.162a3.999 3.999 0 110-7.998 3.999 3.999 0 010 7.998zm6.406-11.845a1.44 1.44 0 11-2.881 0 1.44 1.44 0 012.881 0z"/>
            </svg>
          </a>
        </div>
      </div>

    </div>

    <!-- Bottom copyright -->
    <div class="bg-red-800 text-gray-200 text-sm text-center py-4">
      © 2025 PizzaPan. All rights reserved.
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
</style>
