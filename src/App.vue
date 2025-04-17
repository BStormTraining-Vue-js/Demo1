<script setup>
import { onMounted, ref } from 'vue';
// const count = ref(42);
let countWithoutRef = 42;

onMounted(() => {
//   setInterval(() => {
//     count.value++;
//   }, 1000);

  setInterval(() => {
    countWithoutRef++;
  }, 1000);
});
</script>

<template>
    <!-- <p>Avec ref {{ count }}</p> -->
    <p>Sans ref {{ countWithoutRef }}</p>
</template>

<style scoped>
</style>

