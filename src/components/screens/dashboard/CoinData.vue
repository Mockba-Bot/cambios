<script setup lang="ts">
defineProps<{
  coin: string;
  balance: number;
}>();
</script>

<template>
  <div class="bg-[#252832] py-4 border-b border-[#3A3D4A]">
    <div class="max-w-[375px] mx-auto">
      <div class="flex justify-between px-6">
        <div class="inline-flex items-center gap-3">
          <slot name="icon" />
          <span class="text-3xl">{{ coin }}</span>
        </div>
        <span class="text-3xl">{{ balance }}</span>
      </div>

      <div class="flex justify-between px-6 mt-8">
        <button
          class="bg-linear-90 from-[#D64059] to-[#5E489D] text-white font-bold px-8 py-3 rounded-3xl text-xl cursor-pointer"
        >
          Depositar
        </button>

        <button
          class="text-white font-bold py-3 rounded-3xl text-xl cursor-pointer"
        >
          Retirar
        </button>
      </div>
    </div>
  </div>
</template>
