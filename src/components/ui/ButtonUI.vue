<script setup lang="ts">
defineProps<{
  fullRounded?: boolean;
  fullWidth?: boolean;
}>();
</script>

<template>
  <button
    class="bg-linear-90 from-[#D64059] to-[#5E489D] text-white font-bold px-16 py-3.5 rounded-lg"
    :class="{
      '!rounded-full': fullRounded,
      'w-full': fullWidth,
    }"
  >
    <slot />
  </button>
</template>
