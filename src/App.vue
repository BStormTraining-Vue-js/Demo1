<script setup>
import { computed, ref } from 'vue';

const number = ref(null);
const double = computed(() => number.value + 10);
</script>
 
<template>
    <div>
        <p>Input sans modificateur</p>
        <input v-model="number">
    </div>
    <div>
        <p>Input avec modificateurs</p>
        <input v-model.lazy.number="number">
    </div>
    <p>double : {{ double }}</p>
</template>

<style scoped>

</style>