<script setup>
const keyUpEnterHanler = (event) => {
    // inutile d'ajouter 
    // if (event.key === 'Enter') 
        alert(event.target.value);
};
</script>

<template>
    <input type="text" @keyup.enter="keyUpEnterHanler" placeholder="Appuyer sur Entrée" />
</template>

<style scoped>

</style>

