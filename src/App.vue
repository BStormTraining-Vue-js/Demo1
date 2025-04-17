<script setup>
import { onMounted, ref, useTemplateRef, nextTick } from 'vue';
const text = ref('Khun');
const paragraphe = useTemplateRef('paragraphe');
onMounted(() => {
    setTimeout(async () => {
        text.value = 'Aude';
        // le paragraphe du DOM n'est pas encore mis à jour
        console.log(paragraphe.value.innerText);
        await nextTick();
        // le paragraphe du DOM est mis à jour
        console.log(paragraphe.value.innerText);
    }, 1000);
});
</script>

<template>
    <p ref="paragraphe">{{ text }}</p>
</template>

<style scoped>
    p {
        width: 100px;
    }
</style>

