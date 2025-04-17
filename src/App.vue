<script setup>
import { computed, ref } from 'vue';
const isStPatrick = ref(true);
const style = computed(() => ({
    backgroundColor: isStPatrick ? 'green' : 'blue',
    color: 'white',
    fontSize: '16px',
    padding: '10px',
    borderRadius: '5px',
}));
</script>

<template>
    <p :style>Hello world !!</p>
</template>

<style scoped>

</style>

