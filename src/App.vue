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
    <div class="attribution pt-10 animate-main-secondry -mb-10">
      Challenge by
      <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
      Coded by <a href="#">AbubakerSallam</a>.
    </div>
    <FotterSection />
  </div>
</template>

<style scoped></style>
