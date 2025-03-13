<script setup lang="ts">
import { useRouter } from 'vue-router';

defineProps<{
  openMenu?: boolean;
}>();

const router = useRouter();
</script>

<template>
  <aside
    class="bg-[#1D2025] fixed w-full h-dvh top-0 z-40 transition-all duration-500 ease-in-out"
    :class="{ 'left-0': openMenu, '-left-full': !openMenu }"
  >
    <div class="max-w-[375px] mx-auto px-4 pt-16">
      <nav class="flex flex-col items-center gap-16 mt-4">
        <router-link to="/perfil" class="text-4xl font-light">
          Perfil
        </router-link>
        <router-link to="/" class="text-4xl font-light"> Wallet </router-link>
        <router-link to="/" class="text-4xl font-light"> P2P </router-link>
        <router-link to="/" class="text-4xl font-light"> Ofertas </router-link>
      </nav>

      <div class="flex mt-16" @click="router.push('/')">
        <button
          class="bg-linear-90 from-[#D64059] to-[#5E489D] text-white font-bold px-16 py-3.5 rounded-full w-full text-xl cursor-pointer"
        >
          Cerrar Sesión
        </button>
      </div>
    </div>
  </aside>
</template>
