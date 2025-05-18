<script setup lang="ts">
import { reactive, watch } from 'vue';
const obj = reactive({ nom: 'Khun', age: 43, adresse: { rue: 'Chemin des devs', ville: 'Bruxelles' } });
watch(obj, () => {
    console.log('Le nom ou l\'âge a changé');
})
watch(() => obj.age, () => {
    console.log('L\'âge a changé');
})
watch(() => obj.adresse, () => {
    console.log('Ne se déclenche ici qu\'avec deep: true');
}, /*{ deep: true }*/)
</script>
 
<template>
    <div>
        <input v-model="obj.nom">
        <input v-model="obj.age">
        <input v-model="obj.adresse.ville">
    </div>
</template>

<style scoped>

</style>