<script setup>
import { ref, onMounted } from 'vue'

const isSmallScreen = ref(false)

onMounted(() => {
  const mql = window.matchMedia('(min-width: 640px)')
  isSmallScreen.value = mql.matches
  mql.addEventListener('change', (e) => {
    isSmallScreen.value = e.matches
  })
})
</script>
<template>
  <section class="flex flex-col sm:flex-row w-full">
    <div class="w-1/2 flex items-center mx-auto">
      <img
        class="animate-fade-in-scale scale-150 sm:mt-16 mb-16 backdrop-shadow-3xl w-full sm:-translate-x-42 sm:-translate-y-1/4"
        :src="
          isSmallScreen
            ? 'assets/images/illustration-laptop-desktop.svg'
            : 'assets/images/illustration-laptop-mobile.svg '
        "
      />
    </div>
    <div
      class="z-3 w-1/2 flex flex-col gap-8 sm:gap-19 mx-auto sm:my-0 content-center mt-4 sm:mt-0 animate-main-header max-sm:text-center"
    >
      <div>
        <h1 class="animate-main-secondry text-xl sm:text-3xl font-semibold mb-4">
          Free, open, simple
        </h1>
        <p class="text-sm sm:text-base text-center sm:text-left max-w-lg -mx-10 sm:m-0">
          Blogr is a free and open source application backed by a large community of helpful
          developers. It supports features such as code syntax highlighting, RSS feeds, social media
          integration, third-party commenting tools, and works seamlessly with Google Analytics. The
          architecture is clean and is relatively easy to learn.
        </p>
      </div>
      <div>
        <h1 class="text-xl sm:text-3xl font-semibold mb-4 animate-main-secondry">
          Powerful tooling
        </h1>
        <p class="text-sm sm:text-base text-center sm:text-left max-w-lg -mx-10 sm:m-0">
          Batteries included. We built a simple and straightforward CLI tool that makes
          customization and deployment a breeze, but capable of producing even the most complicated
          sites.
        </p>
      </div>
    </div>
  </section>
</template>
