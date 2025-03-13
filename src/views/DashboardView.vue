<script setup lang="ts">
import HamburgerMenuIcon from '@/components/icons/HamburgerMenuIcon.vue';
import CoinData from '@/components/screens/dashboard/CoinData.vue';
</script>

<template>
  <header class="max-w-[375px] mx-auto px-4 pt-6">
    <button>
      <HamburgerMenuIcon />
    </button>

    <h2 class="font-bold text-3xl mt-6">Balances</h2>

    <div
      class="bg-linear-90 from-[#D64059] to-[#5E489D] rounded-[20px] flex flex-col items-center justify-center gap-4 py-2 mt-2.5"
    >
      <h3 class="text-lg">AVAILABLE ASSETS</h3>

      <span class="text-4xl">$1,000,000</span>
    </div>
  </header>

  <main class="pt-4">
    <div class="bg-[#2B2F3B]">
      <div class="flex justify-between px-6 py-4 max-w-[375px] mx-auto">
        <span class="text-2xl">Asset/Chain</span>
        <span class="text-2xl">Balance</span>
      </div>
    </div>

    <CoinData />
  </main>
</template>
