<script setup lang="ts">
import CardUI from '@/components/ui/CardUI.vue';
import { useRouter } from 'vue-router';

const router = useRouter();
</script>

<template>
  <main class="max-w-[375px] mx-auto px-4">
    <CardUI
      title="Ingresar con frase semilla"
      type="email"
      placeholder="Ingrese tu frase semilla"
      button-text="Continuar"
      @on-submit="router.push('/dashboard')"
    />
  </main>
</template>
