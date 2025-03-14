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
  <aside
    class="bg-[#1D2025] fixed w-full h-dvh top-0 z-40 transition-all duration-500 ease-in-out"
    :class="{ 'left-0': openMenu, '-left-full': !openMenu }"
  >
    <div class="max-w-[375px] mx-auto px-4">
      <div class="flex px-4 pt-6">
        <button @click="closeMenu" class="cursor-pointer">
          <CloseMenuIcon />
        </button>
      </div>
      <nav class="flex flex-col items-center gap-16 mt-8">
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
