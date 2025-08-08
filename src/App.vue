<script setup>
import introNav from './components/introNav.vue'
import HeaderSection from './components/HeaderSection.vue'
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
  <div class="flex flex-col max-w-screen overflow-hidden">
    <introNav :navItems="navItems" />
    <HeaderSection />
    <section class="h-[400px] mb-69 w-screen">
      <div
        class="w-full h-full bg-body-gradient rounded-bl-[96px] relative rounded-tr-[96px] overflow-hidden flex"
      >
        <div class="w-1/2">
          <img
            class="absolute -bottom-1/3 -left-1/6"
            src="./assets/images/bg-pattern-circles.svg"
            alt=""
          />
          <div class="static overflow-visible">
            <img
              class="z-2 absolute overflow-y-scroll left-20 -top-20"
              src="./assets/images/illustration-phones.svg "
              alt=""
            />
          </div>
        </div>
        <div class="z-3 w1/2 mx-auto content-center">
          <h1 class="text-white text-3xl mb-4">State of the Art Infrastructure</h1>
          <p class="text-white max-w-lg">
            With reliability and speed in mind, worldwide data centers provide the backbone for
            ultra-fast connectivity. This ensures your site will load instantly, no matter where
            your readers are, keeping your site competitive.
          </p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped></style>
