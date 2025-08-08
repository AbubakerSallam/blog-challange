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
  <div class="max-w-screen mb-20 sm:mb-0 mt-20 mx-auto">
    <div class="font-bold text-3xl text-center">Designed for the future</div>

    <div
      class="flex flex-col-reverse text-center sm:text-left mx-auto justify-around sm:flex-row max-w-screen"
    >
      <div class="sm:w-2/3 space-y-8 mt-16 sm:ml-42 justify-center">
        <div class="text-xl font-semibold mx-auto max-sm:max-w-4/5 items-center">
          <span class="inline-flex max-sm:max-w-2/3">Introducing an extensible editor</span>
          <p class="max-w-lg text-base font-normal mt-2">
            Blogr features an exceedingly intuitive interface which lets you focus on one thing:
            creating content. The editor supports management of multiple blogs and allows easy
            manipulation of embeds such as images, videos, and Markdown. Extensibility with plugins
            and themes provide easy ways to add functionality or change the looks of a blog.
          </p>
        </div>

        <div class="text-xl max-sm:max-w-4/5 mx-auto font-semibold block">
          <span class="inline-flex max-sm:max-w-2/3">Robust content management</span>
          <p class="max-w-lg text-base font-normal mt-2">
            Flexible content management enables users to easily move through posts. Increase the
            usability of your blog by adding customized categories, sections, format, or flow. With
            this functionality, you’re in full control.
          </p>
        </div>
      </div>

      <div class="sm:-translate-y-14 w-full overflow-hidden">
        <img
          class="backdrop-shadow-3xl w-full sm:translate-x-1/4"
          :src="
            isSmallScreen
              ? './src/assets/images/illustration-editor-desktop.svg'
              : './src/assets/images/illustration-editor-mobile.svg'
          "
          alt=""
        />
      </div>
    </div>
  </div>
</template>
