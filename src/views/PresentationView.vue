<script setup lang="ts"></script>

<template>
  <main class="min-h-dvh min-w-dvw relative overflow-hidden">
    <div
      class="absolute bg-linear-90 from-[#D64059] to-[#5E489D] w-[350px] sm:w-[500px] h-[350px] sm:h-[500px] rounded-full top-[-5%] lg:top-[-10%] left-[-25%] lg:left-[-10%] blur-[60px] -z-50"
    ></div>

    <div class="absolute inset-0 grid place-content-center">
      <h1 class="text-6xl syncopate-bold">CAMBIOS</h1>
      <h2 class="indent-1.5 text-xl syncopate-regular">DEXCHANGE</h2>

      <div class="mx-auto mt-10">
        <RouterLink
          to="/"
          class="bg-linear-90 from-[#D64059] to-[#5E489D] text-white font-bold px-16 py-3.5 rounded-full w-max"
        >
          Iniciar APP
        </RouterLink>
      </div>
    </div>

    <div
      class="absolute bg-linear-90 from-[#D64059] to-[#5E489D] w-[350px] sm:w-[500px] h-[350px] sm:h-[500px] rounded-full bottom-[-5%] lg:bottom-[-10%] right-[-25%] lg:right-[-10%] blur-[60px] -z-50"
    ></div>
  </main>
</template>
