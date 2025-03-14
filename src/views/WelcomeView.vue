<script setup lang="ts"></script>

<template>
  <main class="mt-20 max-w-[375px] mx-auto px-4">
    <div class="flex">
      <h1 class="text-4xl tracking-wide">Bienvenido</h1>
    </div>

    <div class="mt-10 flex justify-center">
      <img src="/robot.png" class="h-[180px]" alt="" />
    </div>

    <div class="flex flex-col gap-12 items-center justify-center">
      <RouterLink
        to="/registro"
        class="bg-linear-90 from-[#D64059] to-[#5E489D] text-white font-bold py-3.5 rounded-lg w-full flex justify-center"
      >
        Registro
      </RouterLink>
      <RouterLink
        to="/login-with-seedphrase"
        class="bg-linear-90 from-[#D64059] to-[#5E489D] text-white font-bold px-16 py-3.5 rounded-lg w-full flex justify-center"
      >
        Ingresar con frase semilla
      </RouterLink>
      <RouterLink
        to="/login"
        class="bg-linear-90 from-[#D64059] to-[#5E489D] text-white font-bold px-16 py-3.5 rounded-lg w-full flex justify-center"
      >
        Ingresar con correo
      </RouterLink>
    </div>
  </main>
</template>
