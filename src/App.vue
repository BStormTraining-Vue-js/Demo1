<script setup lang="ts">
import { onMounted, useTemplateRef } from 'vue';

const listItems = useTemplateRef('li');
const ingredients = ['sel', 'poivre', 'sucre'];
onMounted(() => {
    console.log(listItems.value); // [li, li, li]
})
</script>
 
<template>
    <ul>
        <li v-for="item in ingredients" ref="li"> {{ item }}</li>
    </ul>
</template>

<style scoped>

</style>