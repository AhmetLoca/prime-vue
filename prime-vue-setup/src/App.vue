<script setup>
import { ref } from "vue";
import { useToast } from "primevue/usetoast";

const text = ref();
const toast = useToast();

const greet = () => {
  toast.add({
    severity: "info",
    summary: "Onaylandi",
    detail: "Message Content",
    life: 1500,
  });
};
</script>

<template>
  <Toast position="bottom-center" />
  <h1>Welcome to PrimeTime</h1>

  <div class="container">
    <span class="p-float-label p-input-filled" style="margin-right: 1rem">
      <InputText id="txt" type="text" v-model="text" />
      <label for="txt">Username</label>
    </span>
    <Button label="Greet" @click="greet" icon="pi pi-user"></Button>
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
