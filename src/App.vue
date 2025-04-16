<script setup>
import { ref } from 'vue';
const rawHTML = ref('<a href="https://www.google.be">Google</a>');
</script>

<template>
    <!-- HTML échappé -->
    <p>Lien vers {{ rawHTML }} !</p>
    <!-- HTML non échappé -->
    <p>Lien vers <span v-html="rawHTML"></span>!</p>
</template>

<style scoped>
div{
    font-size: 20px;
}
</style>

