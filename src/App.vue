<script setup>
import introNav from './components/introNav.vue'
import HeaderSection from './components/HeaderSection.vue'
import middleSection from './components/middleSection.vue'
import { ref } from 'vue'
import LaptopSection from './components/laptopSection.vue'
import FotterSection from './components/fotterSection.vue'
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
  <div class="flex flex-col max-w-screen overflow-hidden">
    <introNav :navItems="navItems" />
    <HeaderSection />
    <middleSection />
    <LaptopSection />
    <FotterSection />
  </div>
</template>

<style scoped></style>
