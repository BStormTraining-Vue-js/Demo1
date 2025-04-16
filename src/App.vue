<script setup>
const attributes = {
    disabled: true,
    type: 'reset',
    class: 'btn-red',
};
</script>

<template>
    <button v-bind="attributes">Click Me</button>
</template>

<style scoped>
.btn-red {
    background-color: red;
    color: white;
}
.btn-red:disabled {
    opacity: 0.5;
}
</style>

