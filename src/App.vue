<script setup>
import { ref } from 'vue';
const name = ref('world');
</script>

<template>
    <p>Hello {{ name }} !!</p>
</template>

<style scoped>
div{
    font-size: 20px;
}
</style>

