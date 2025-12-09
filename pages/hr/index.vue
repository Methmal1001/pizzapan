<template>
  <div class="min-h-screen bg-gray-100 dark:bg-gray-900 p-8">
    <!-- Page Header -->
    <h1 class="text-3xl font-bold mb-8 text-gray-800 dark:text-white">HR Dashboard</h1>

    <!-- Search Section -->
    <div class="mb-8 flex flex-col sm:flex-row gap-4 items-center">
      <input
        v-model="searchQuery"
        type="text"
        placeholder="Search by Employee No or Name"
        class="flex-1 p-3 rounded-xl border border-gray-300 focus:outline-none focus:ring-2 focus:ring-red-500 dark:bg-gray-800 dark:text-white dark:border-gray-600"
      />
      <button
        @click="searchEmployee"
        class="bg-red-600 hover:bg-red-700 text-white px-6 py-3 rounded-xl font-semibold transition-all"
      >
        Search
      </button>
    </div>

    <!-- Dashboard Cards -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 mb-8">
      <!-- OT Details Card -->
      <div class="bg-gradient-to-br from-red-700 to-yellow-500 p-6 rounded-2xl shadow-2xl transform hover:scale-105 hover:shadow-xl transition-all flex flex-col items-center text-white cursor-pointer">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mb-2" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
        </svg>
        <span class="font-bold text-lg">OT Details</span>
        <span class="mt-1 text-sm">Track employee overtime</span>
      </div>

      <!-- Rectifications Card -->
      <div class="bg-gradient-to-br from-red-700 to-yellow-500 p-6 rounded-2xl shadow-2xl transform hover:scale-105 hover:shadow-xl transition-all flex flex-col items-center text-white cursor-pointer">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mb-2" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
        </svg>
        <span class="font-bold text-lg">Rectifications</span>
        <span class="mt-1 text-sm">View pending corrections</span>
      </div>

      <!-- Leaves Card -->
      <div class="bg-gradient-to-br from-red-700 to-yellow-500 p-6 rounded-2xl shadow-2xl transform hover:scale-105 hover:shadow-xl transition-all flex flex-col items-center text-white cursor-pointer">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mb-2" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7H3v12a2 2 0 002 2z" />
        </svg>
        <span class="font-bold text-lg">Leaves</span>
        <span class="mt-1 text-sm">Approve or track leaves</span>
      </div>
    </div>

    <!-- Employee Cards -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div
        v-for="emp in filteredEmployees"
        :key="emp.empNo"
        class="bg-white dark:bg-gray-800 p-6 rounded-2xl shadow-lg hover:shadow-xl transition-all"
      >
        <div class="flex justify-between items-center mb-2">
          <span class="font-bold text-lg text-gray-800 dark:text-white">{{ emp.name }}</span>
          <span class="text-sm text-gray-500 dark:text-gray-400">{{ emp.empNo }}</span>
        </div>

        <div class="grid grid-cols-2 gap-4 mt-4">
          <div class="bg-red-100 dark:bg-red-800 p-3 rounded-xl text-center">
            <span class="font-semibold text-red-700 dark:text-red-300">OT Hours</span>
            <p class="mt-1 text-lg font-bold text-gray-800 dark:text-white">{{ emp.otHours }}</p>
          </div>
          <div class="bg-yellow-100 dark:bg-yellow-800 p-3 rounded-xl text-center">
            <span class="font-semibold text-yellow-700 dark:text-yellow-300">Rectifications</span>
            <p class="mt-1 text-lg font-bold text-gray-800 dark:text-white">{{ emp.rectifications }}</p>
          </div>
          <div class="bg-red-100 dark:bg-red-800 p-3 rounded-xl text-center col-span-2">
            <span class="font-semibold text-red-700 dark:text-red-300">Leaves</span>
            <p class="mt-1 text-lg font-bold text-gray-800 dark:text-white">{{ emp.leaves }}</p>
          </div>
        </div>
      </div>

      <div v-if="filteredEmployees.length === 0" class="col-span-full text-center text-gray-500 dark:text-gray-400 mt-4">
        No employees found.
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

const searchQuery = ref('')

// Example employee data
const employees = ref([
  { empNo: 'E001', name: 'John Doe', otHours: 5, rectifications: 2, leaves: 1 },
  { empNo: 'E002', name: 'Jane Smith', otHours: 3, rectifications: 0, leaves: 2 },
  { empNo: 'E003', name: 'Mike Johnson', otHours: 8, rectifications: 1, leaves: 0 },
])

const searchEmployee = () => {
  console.log('Search triggered for:', searchQuery.value)
}

const filteredEmployees = computed(() => {
  if (!searchQuery.value) return employees.value
  return employees.value.filter(
    emp =>
      emp.empNo.toLowerCase().includes(searchQuery.value.toLowerCase()) ||
      emp.name.toLowerCase().includes(searchQuery.value.toLowerCase())
  )
})
</script>

<style>
/* Optional: Smooth hover transition */
</style>
