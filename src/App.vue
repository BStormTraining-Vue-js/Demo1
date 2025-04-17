<script setup>
import { onMounted, ref } from 'vue';
const isLoggedIn = ref(false);

onMounted(() => {
    setInterval(() => {
        isLoggedIn.value = true;
    }, 2000);
});
</script>

<template>
    <button v-show="!isLoggedIn">Login</button>
    <button v-show="isLoggedIn">Logout</button>
</template>

<style scoped>

</style>

