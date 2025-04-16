<script setup>
import { ref } from 'vue';
const disabled = ref(true);
</script>

<template>
    <button :disabled="disabled">Click Me</button>
    <!-- Si le nom de l'attribut est identique au nom de la variable JavaScript -->
    <button :disabled>Click Me</button>
</template>

<style scoped>
div{
    font-size: 20px;
}
</style>

