<script setup>
const log = console.log
</script>

<template>
    <!-- se déclenchera si la touche enter est relevée -->
    <input @keyup.enter="log('enter')">
    <!-- se déclenchera si les touches alt et enter sont baissées -->
    <input @keydown.alt.enter="log('alt + enter')">
    <!-- se déclenchera si la touche ctrl est baissée au moment du click  -->
    <p @click.ctrl="log('click + ctrl')">Cliquer ici sur en appuyant sur enter en même temps</p>
</template>

<style scoped>

</style>