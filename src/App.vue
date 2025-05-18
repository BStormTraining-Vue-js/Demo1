<script setup lang="ts">
import { onMounted, useTemplateRef } from 'vue';

const paragraphe = useTemplateRef('p');
console.log(paragraphe.value); // null
onMounted(() => {
    console.log(paragraphe.value); // <p>Some text ...</p>
})
</script>
 
<template>
    <p ref="p">Some text ...</p>
</template>

<style scoped>

</style>