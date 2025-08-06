<script setup>
import introNav from './components/introNav.vue'
import { ref } from 'vue'
const navItems = ref([
  {
    navName: 'Product',
    items: [' Overview', 'Pricing', 'Marketplace', 'Features', 'Integrations'],
  },
  {
    navName: 'Company',
    items: [' About', '  Team', '  Blog', 'Careers'],
  },
  {
    navName: 'Connect',
    items: [' Contact', 'Newsletter', 'LinkedIn'],
  },
])
</script>

<template>
  <div class="flex flex-col h-screen max-w-screen">
    <introNav :navItems="navItems" />
  </div>
</template>

<style scoped></style>
