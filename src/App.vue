<script setup>
const leftClick = () => {
    alert('Vous avez cliquez sur le bouton gauche !');
};
const rightClick = () => {
    alert('Vous avez cliquez sur le bouton droit !');
};
</script>

<template>
    <button @click.left="leftClick" @click.right.prevent="rightClick">Click me !</button>
</template>

<style scoped>

</style>