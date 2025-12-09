<template>
  <div>
    <Header />
    <main class="pt-16">
      <slot />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Header from '~/components/project/header.vue'
import Footer from '~/components/project/footer.vue'
</script>
<style></style>