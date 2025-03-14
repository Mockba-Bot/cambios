<script setup lang="ts">
import { ref } from 'vue';

import HamburgerMenuIcon from '@/components/icons/HamburgerMenuIcon.vue';
import CoinData from '@/components/screens/dashboard/CoinData.vue';
import NavBar from '@/components/screens/dashboard/NavBar.vue';

const openMenu = ref(false);
</script>

<template>
  <header class="max-w-[375px] mx-auto px-4 pt-6">
    <button @click="openMenu = true" class="cursor-pointer">
      <HamburgerMenuIcon />
    </button>

    <h2 class="font-bold text-3xl mt-8">Balances</h2>

    <div
      class="bg-linear-90 from-[#D64059] to-[#5E489D] rounded-[20px] flex flex-col items-center justify-center gap-2 py-2 mt-2.5"
    >
      <h3 class="text-lg">Disponible</h3>

      <span class="text-2xl">$1,000,000</span>
    </div>
  </header>

  <main class="pt-4">
    <div class="bg-[#2B2F3B]">
      <div class="flex justify-between px-6 py-4 max-w-[375px] mx-auto">
        <span class="text-xl">Asset/Chain</span>
        <span class="text-xl">Balance</span>
      </div>
    </div>

    <CoinData coin="Arbitrum" :balance="100">
      <template #icon>
        <img src="/arbitrum-arb-logo.svg" alt="Arbitrum" class="w-8 h-8" />
      </template>
    </CoinData>
    <CoinData coin="USDT" :balance="100">
      <template #icon>
        <img src="/tether-usdt-logo.svg" alt="Arbitrum" class="w-8 h-8" />
      </template>
    </CoinData>
    <CoinData coin="USDC" :balance="100">
      <template #icon>
        <img src="/usd-coin-usdc-logo.svg" alt="Arbitrum" class="w-8 h-8" />
      </template>
    </CoinData>
  </main>

  <NavBar :open-menu="openMenu" @update:closeMenu="openMenu = false" />
</template>
