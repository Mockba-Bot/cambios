<script setup lang="ts">
import { useRouter } from 'vue-router';

const router = useRouter();
</script>

<template>
  <main class="max-w-[375px] mx-auto px-4">
    <div class="flex justify-center mt-20">
      <img src="/robot.png" class="h-[180px]" alt="" />
    </div>

    <form @submit.prevent class="bg-[#2B2F3B] rounded-2xl py-8 px-6">
      <h2 class="text-xl">Editar perfil</h2>

      <div class="mt-6">
        <label for="name" class="block text-sm font-medium"> Nombre: </label>
        <input
          type="text"
          id="name"
          name="name"
          class="mt-2 block w-full px-3 py-2 rounded-lg bg-[#252832]"
          required
        />
      </div>

      <div class="mt-6">
        <label for="lastName" class="block text-sm font-medium">
          Apellido:
        </label>
        <input
          type="text"
          id="lastName"
          name="lastName"
          class="mt-2 block w-full px-3 py-2 rounded-lg bg-[#252832]"
          required
        />
      </div>

      <div class="mt-6">
        <label for="email" class="block text-sm font-medium">
          Correo electrónico:
        </label>
        <input
          type="email"
          id="email"
          name="email"
          class="mt-2 block w-full px-3 py-2 rounded-lg bg-[#252832]"
          required
        />
      </div>

      <div class="mt-6">
        <label for="telegram" class="block text-sm font-medium">
          Telegram:
        </label>
        <input
          type="text"
          id="telegram"
          name="telegram"
          class="mt-2 block w-full px-3 py-2 rounded-lg bg-[#252832]"
          required
        />
      </div>

      <button
        class="mt-12 bg-linear-90 from-[#D64059] to-[#5E489D] text-white font-bold py-2 w-full rounded-lg text-sm cursor-pointer"
        type="submit"
        @click="router.push('/dashboard')"
      >
        Continuar
      </button>
    </form>
  </main>
</template>
