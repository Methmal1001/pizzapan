<template>
  <div class="min-h-screen bg-gray-100 dark:bg-gray-900 p-8">
    <h1 class="text-3xl font-bold mb-8 text-gray-800 dark:text-white">Pizza Shop Dashboard</h1>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
      <DashboardCard
        title="HR Portal"
        description="Manage employees and attendance"
        icon="/images/hr.png"
        @click="navigate('hr')"
      />
      <DashboardCard
        title="Sales Portal"
        description="Track orders and revenue"
        icon="/images/sales.png"
        @click="navigate('sales')"
      />
      <DashboardCard
        title="Marketing"
        description="Campaigns and promotions"
        icon="/images/marketing.png"
        @click="navigate('marketing')"
      />
      <DashboardCard
        title="Billing Portal"
        description="Invoices and payments"
        icon="/images/billing.png"
        @click="navigate('billing')"
      />
    </div>
  </div>
</template>

<script setup>
import DashboardCard from '~/components/DashboardCard.vue'
import { useRouter } from 'vue-router'

const router = useRouter()
const navigate = (page) => {
  router.push(`/${page}`)
}
</script>
