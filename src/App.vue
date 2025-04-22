<script setup>
import { ref } from 'vue';
const count = ref(0);
const increase = () => {
    count.value++;
}
</script>

<template>
    <p>Compteur : {{ count }}</p>
    <button @click="increase">+</button>
</template>

<style scoped>
div{
    font-size: 20px;
}
</style>

