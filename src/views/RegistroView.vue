<script setup lang="ts">
import { ref } from 'vue';
import EmailView from '@/components/screens/register/EmailView.vue';

const currentStep = ref(1);
</script>

<template>
  <main class="max-w-[375px] mx-auto px-4">
    <EmailView v-if="currentStep === 1" />
  </main>
</template>
