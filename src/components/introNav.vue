<script setup>
import menueicon from '../assets/icons/menue.svg'
import closemenue from '../assets/icons/closemenue.svg'
import { ref, onMounted } from 'vue'

const navopend = ref('')
const showMenue = ref(false)
const isSmallScreen = ref(false)
const props = defineProps({
  navItems: Object,
  required: true,
})
onMounted(() => {
  const mql = window.matchMedia('(min-width: 640px)')
  isSmallScreen.value = mql.matches
  mql.addEventListener('change', (e) => {
    isSmallScreen.value = e.matches
  })
})
const toggleShowMenue = () => {
  showMenue.value = !showMenue.value
}
const opennav = (index) => {
  if (navopend.value === props.navItems[index].navName) {
    navopend.value = ''
  } else navopend.value = props.navItems[index].navName
}
</script>
<template>
  <section
    class="flex text-white flex-col h-96 pb-[430px] sm:h2/3 rounded-bl-[64px] bg-gradient-to-r from-orange-300 to-red-550 relative sm:overflow-hidden"
  >
    <div
      class="absolute top-0 w-screen h-full bg-[url('./src/assets/images/bg-pattern-intro-mobile.svg')] sm:bg-[url('./src/assets/images/bg-pattern-intro-desktop.svg')] bg-no-repeat bg-[26%_center] z-0"
    ></div>

    <nav class="flex relative mx-4 sm:mx-18 my-8 justify-between">
      <img class="pr-12 h-full" src="../assets/images/logo.svg" alt="" />
      <!-- <h1 class="text-white text-3xl font-bold inline pr-12">Bloger</h1> -->
      <div
        :class="{
          'hidden  sm:flex   ': !showMenue,
          'text-gray-900   items-center  max-sm:absolute z-10   text-center space-y-2 max-sm:min-w-full max-sm:mt-13 max-sm:top-4  max-sm:-bottom-150  max-sm:bg-white rounded-lg max-sm:shadow-2xl  max-sm:p-10   ':
            showMenue,
        }"
        class="items-center flex-row sm:flex sm:flex-1 sm:text-white"
      >
        <div class="sm:relative flex justify-center" v-for="(item, index) in navItems" :key="index">
          <div class="sm:space-x-4">
            <div
              @click="opennav(index)"
              class="cursor-pointer pr-3 hover:underline underline-offset-1 font-semibold"
            >
              {{ item.navName }}

              <img
                :class="`${item.navName}` === navopend ? 'rotate-180' : ''"
                class="inline w-4 font-semibold pl-1 duration-300 transition-all"
                :src="
                  isSmallScreen
                    ? './src/assets/images/icon-arrow-light.svg'
                    : './src/assets/images/icon-arrow-dark.svg'
                "
                alt="Arrow Icon"
              />
            </div>
            <div
              id="product"
              :class="`${item.navName}` === navopend ? 'flex' : 'hidden'"
              class="z-10 sm:absolute transition-transform duration-500 transform-content top-10 max-sm:px-20 bg-gray-100 flex-col sm:-translate-x-[65%] sm:left-1/2 py-4 px-5 space-y-1 sm:bg-white rounded-lg shadow-2xl"
            >
              <ul v-for="subItem in item.items">
                <li
                  @click="navopend = ''"
                  class="text-gray-900 hover:font-bold cursor-pointer transition-all delay-100 duration-300"
                >
                  {{ subItem }}
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div
          :class="{
            'hidden sm:flex ': !showMenue,
            '  flex-col   ': showMenue,
          }"
          class="items-center mt-16 sm:mt-0 border-t-1 border-gray-400 sm:border-none pt-3 sm:pt-0 sm:ml-auto flex sm:gap-2 sm:flex-row"
        >
          <a href="#" class="font-semibold px-4 py-3 rounded-2xl text-gray-900 sm:text-white">
            Login
          </a>
          <a
            href="#"
            class="font-semibold sm:bg-white px-7 py-2 rounded-full max-sm:bg-gradient-to-r from-orange-300 to-red-550 sm:text-red-600 text-white hover:text-white hover:bg-red-300"
            >Sign Up</a
          >
        </div>
      </div>
      <div class="sm:hidden">
        <closemenue
          v-if="showMenue"
          @click="toggleShowMenue"
          class="fill-current text-white mobile:text-red w-8 sm:hidden cursor-pointer"
        />
        <menueicon
          v-else
          @click="toggleShowMenue"
          class="fill-current text-white mobile:text-red w-8 sm:hidden cursor-pointer"
        />
      </div>
    </nav>
    <div class="z-1 mt-16 justify-between items-center text-center">
      <span class="text-4xl font-bold block sm:inline-flex">A modern&nbsp;</span>
      <span class="text-4xl font-bold">publishing platform</span>
      <p class="mt-4 mx-auto max-sm:max-w-xs">Grow your audience and build your online brand</p>

      <div class="mt-10 flex-row space-x-3 justify-between">
        <a
          href="#"
          class="font-semibold bg-white px-5 py-3 rounded-full text-red-600 hover:text-white hover:bg-red-300"
          >Start for Free</a
        >
        <a href="#" class="font-semibold px-5 py-3 rounded-full text-white border border-white">
          Learn More
        </a>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped></style>
