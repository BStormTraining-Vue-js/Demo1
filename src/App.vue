<script setup>
const clickHandler = (event) => {
    console.log(event);
    alert("Vous avez cliqué sur le bouton !");
};
</script>

<template>
    <button v-on:click="clickHandler">Click me!</button>
    <!-- forme raccourcie -->
    <button @click="clickHandler">Click me!</button>
</template>

<style scoped>

</style>

