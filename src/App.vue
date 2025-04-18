<script setup>
const clickHandler = (event) => {
    // inutile d'ajouter 
    // event.preventDefault()
    alert('Vous avez cliqué sur le lien ! Sans être redirigé !')
};
</script>

<template>
    <a href="https://google.be" @click.prevent="clickHandler">Google</a>
</template>

<style scoped>

</style>

