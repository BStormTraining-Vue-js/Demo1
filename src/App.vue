<script setup>
import { ref, reactive } from 'vue';
const score = ref(7);
const classes = reactive(['text-white', 'bg-green']);
</script>

<template>
    <p :class="{
        success: score >= 8,
        warning: score >=5 && score < 8,
        danger: score < 5 }"
    >{{ score }}</p>
    <!-- <p class="warning">7</p> -->
    <button :class="classes">Click Me !!</button>
    <!-- <button class="text-white bg-green">Click Me !!</button> -->
</template>

<style scoped>

.success {
    color: green;
}
.warning {
    color: orange;
}
.danger {
    color: red;
}
.text-white {
    color: white;
}
.bg-green {
    background-color: green;
}
</style>

