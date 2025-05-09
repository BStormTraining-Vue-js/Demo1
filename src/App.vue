<script setup>
const middleClick = () => {
    alert('Vous avez cliquez sur le bouton central !');
};
const rightClick = () => {
    alert('Vous avez cliquez sur le bouton droit !');
};
</script>

<template>
    <button @click.middle="middleClick" @click.right.prevent="rightClick">Click me !</button>
</template>

<style scoped>

</style>