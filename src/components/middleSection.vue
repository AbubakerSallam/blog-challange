<template>
  <section class="h-[400px] mt-32 my-16 sm:mb-64 sm:mt-0 w-screen">
    <div
      class="w-full h-full bg-body-gradient animate-fade-in-scale rounded-bl-[96px] relative rounded-tr-[96px] space-y-4 justify-between flex flex-col sm:flex-row overflow-visible"
    >
      <!-- Left Side -->
      <div class="w-1/2 relative">
        <!-- Pattern Circles (clipped inside) -->
        <div class="absolute w-screen inset-0 overflow-hidden">
          <img
            class="animate-main-header -left-1/5 -top-[500px] absolute"
            src="../../public/images/bg-pattern-circles.svg"
            alt=""
          />
        </div>

        <!-- Phones Image (allowed to overflow) -->
        <div class="relative w-full h-full z-10">
          <img
            class="absolute left-1/2 scale-150 sm:scale-100 sm:left-20 -top-20 animate-main-secondry"
            src="../../public/images/illustration-phones.svg"
            alt=""
          />
        </div>
      </div>

      <!-- Right Side Text -->
      <div
        class="z-20 w-1/2 mx-auto my-auto sm:my-0 content-center mt-36 sm:mt-0 animate-main-secondry"
      >
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
