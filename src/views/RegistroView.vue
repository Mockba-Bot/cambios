<script setup lang="ts">
import { ref } from 'vue';
import { useRouter } from 'vue-router';

import CardUI from '@/components/ui/CardUI.vue';

const router = useRouter();
const currentStep = ref(1);
</script>

<template>
  <main class="max-w-[375px] mx-auto px-4">
    <div v-if="currentStep === 1">
      <CardUI
        title="Ingresa con correo"
        type="email"
        placeholder="Ingrese tu correo electrónico"
        button-text="Continuar"
        @onSubmit="currentStep = 2"
      />
    </div>

    <CardUI
      v-else-if="currentStep === 2"
      title="Nombre del respaldo"
      type="text"
      placeholder="Ingrese un nombre para su respaldo"
      button-text="Continuar"
      @onSubmit="currentStep = 3"
    />

    <CardUI
      v-else-if="currentStep === 3"
      title="Ingrese el código de verificación"
      type="text"
      placeholder="Ingrese el código enviado al correo"
      button-text="Verificar"
      @onSubmit="router.push('/dashboard')"
    />
  </main>
</template>
