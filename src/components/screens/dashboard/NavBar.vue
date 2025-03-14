<script setup lang="ts">
import { useRouter } from 'vue-router';

import CloseMenuIcon from '@/components/icons/CloseMenuIcon.vue';

defineProps<{
  openMenu?: boolean;
}>();

const emit = defineEmits(['update:closeMenu']);

const router = useRouter();

function closeMenu() {
  emit('update:closeMenu');
}
</script>

<template>
  <div
    class="bg-[#1D2025]/75 w-screen h-screen z-30 top-0"
    :class="{
      'z-30 opacity-100 fixed': openMenu,
      '-z-50 opacity-0 hidden': !openMenu,
    }"
  ></div>
  <aside
    class="bg-[#1D2025] fixed w-full h-dvh top-0 z-40 transition-all duration-500 ease-in-out"
    :class="{ 'left-[25%]': openMenu, '-left-full': !openMenu }"
  >
    <div class="max-w-[375px] ml-[25%]">
      <div class="flex px-4 pt-6">
        <button @click="closeMenu" class="cursor-pointer">
          <CloseMenuIcon />
        </button>
      </div>
      <nav class="flex flex-col items-center gap-12 mt-8">
        <router-link to="/perfil" class="text-xl font-light">
          Perfil
        </router-link>
        <router-link to="/" class="text-xl font-light"> Wallet </router-link>
        <router-link to="/" class="text-xl font-light"> P2P </router-link>
        <router-link to="/" class="text-xl font-light"> Ofertas </router-link>
      </nav>

      <div class="flex mt-12" @click="router.push('/')">
        <button
          class="bg-linear-90 from-[#D64059] to-[#5E489D] text-white font-bold py-2 rounded-full w-full text-lg cursor-pointer"
        >
          Cerrar Sesión
        </button>
      </div>
    </div>
  </aside>
</template>
