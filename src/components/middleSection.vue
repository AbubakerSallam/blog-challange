<template>
  <section class="h-[400px] my-16 sm:my-64 w-screen">
    <div
      class="w-full h-full bg-body-gradient rounded-bl-[96px] relative rounded-tr-[96px] space-y-4 overflow-hidden justify-between flex flex-col sm:flex-row"
    >
      <!-- TODO: try to add group that may add the overflow hidden to specific div -->
      <div class="w-1/2">
        <img
          class="absolute max-sm:-top-4/12 sm:-bottom-1/3 sm:-left-1/6"
          src="../assets/images/bg-pattern-circles.svg"
          alt=""
        />
        <div class="relative w-full h-full">
          <img
            class="z-2 absolute overflow-visible left-1/2 scale-150 sm:scale-100 sm:left-20 -top-20"
            src="../assets/images/illustration-phones.svg "
            alt=""
          />
        </div>
      </div>
      <div class="z-3 w-1/2 mx-auto my-auto sm:my-0 content-center mt-32 sm:mt-0">
        <h1 class="text-white text-2xl sm:text-3xl font-semibold mb-4">
          State of the Art Infrastructure
        </h1>
        <p
          class="sm:text-white text-zinc-300 text-sm sm:text-base text-center sm:text-left max-w-lg -mx-10 sm:m-0"
        >
          With reliability and speed in mind, worldwide data centers provide the backbone for
          ultra-fast connectivity. This ensures your site will load instantly, no matter where your
          readers are, keeping your site competitive.
        </p>
      </div>
    </div>
  </section>
</template>

<script setup></script>

<style lang="scss" scoped></style>
