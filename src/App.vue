<script setup>
import { onMounted, ref } from 'vue';
const age = ref(1);

onMounted(() => {
    setInterval(() => {
        age.value++;
    }, 250);
});
</script>

<template>
    <p>Age: {{ age }}</p>
    <p v-if="age < 6">🙈</p>
    <p v-else-if="age < 18">🙊</p>
    <p v-else>🙉</p>
</template>

<style scoped>

</style>

