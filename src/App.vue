<script setup>
import { onMounted, reactive } from 'vue';
const counts = reactive([42]);

onMounted(() => {
    setInterval(() => {
        counts.push(counts.at(-1) + 1);
    }, 1000);
});
</script>

<template>
    <p>{{ counts }}</p>
</template>

<style scoped>
</style>

