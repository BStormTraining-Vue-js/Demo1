<script setup>
import { ref } from 'vue';
const name = ref(null);
const text = ref(null);
const checked = ref(false);
const categories = ref([]);
const gender = ref(null);
const country = ref(null);
</script>

<template>
    <!-- sans v-model -->
    <input :value="name" @input="e => name = e.target.value">
    <!-- utilisations basiques -->
    <!-- text -->
    <p>Valeur encodée: {{ name }}</p>
    <hr>
    <input v-model="name">
    <!-- textearea -->
    <p>Valeur encodée: {{ text }}</p>
    <textarea v-model="text"></textarea>
    <hr>
    <!-- checkbox -->
    <p>Valeur encodée: {{ checked }}</p>
    <input type="checkbox" v-model="checked">
    <hr>
    <!-- checkbox multiple -->
    <p>Valeurs encodées: {{ categories }}</p>
    <label for="House">Maison</label>
    <input id="House" type="checkbox" v-model="categories" value="HOUSE">
    <label for="Appartment">Appartement</label>
    <input id="Appartment" type="checkbox" v-model="categories" value="APPARTMENT">
    <label for="Other">Autre</label>
    <input id="Other" type="checkbox" v-model="categories" value="OTHER">
    <hr>
    <!-- radio -->
    <p>Valeur encodée: {{ gender }}</p>
    <label for="Male">Homme</label>
    <input id="Male" type="radio" v-model="gender" value="MALE">
    <label for="Female">Femme</label>
    <input id="Female" type="radio" v-model="gender" value="FEMALE">
    <label for="Other">Autre</label>
    <input id="Other" type="radio" v-model="gender" value="OTHER">
    <hr>
    <!-- select -->
    <p>Valeur encodée: {{ country }}</p>
    <select v-model="country">
        <option value="BE">Belgique</option>
        <option value="FR">France</option>
        <option value="UK">Royaumes unis</option>
    </select>  
</template>

<style scoped>

</style>