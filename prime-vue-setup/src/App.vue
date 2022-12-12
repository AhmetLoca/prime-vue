<script setup>
import { ref } from "vue";
const text = ref();
</script>

<template>
  <h1>Welcome to PrimeTime</h1>
  
  <div class="container">
    <span class="p-float-label">
      <InputText id="txt" type="text" v-model="text" />
      <label for="txt">Username</label>
    </span>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
</style>
