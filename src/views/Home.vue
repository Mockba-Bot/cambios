<template>
  <div class="home">
    <h1>Welcome to Your Vue.js App</h1>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HelloWorld from '@/components/HelloWorld.vue';

export default defineComponent({
  name: 'Home',
  components: {
    HelloWorld,
  },
});
</script>

<style scoped>
.home {
  text-align: center;
}
</style>