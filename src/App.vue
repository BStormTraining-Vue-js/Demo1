<script setup>
import { onMounted, reactive } from 'vue';

const movies = reactive([
    { id: 1, title: 'E.T.'},
    { id: 2, title: 'The Matrix'},
    { id: 3, title: 'The Lord of the Rings'},
]);

onMounted(() => {
    setTimeout(() => {
        movies.push({ id: 4, title: 'Interstellar'});
        movies.unshift({ id: 5, title: 'Inception'});
    }, 2000);
});
</script>

<template>
    <p>Sans tracking</p>
    <ul>
        <li v-for="(item, i) in movies">{{ item.title }} (index : {{ i }})</li>
    </ul>
    <hr>
    <p>Avec tracking</p>
    <ul>
        <li v-for="(item, i) in movies" :key="item.id">{{ item.title }} (index : {{ i }})</li>
    </ul>
</template>

<style scoped>
    @keyframes appearing {
        0% { opacity: 0; transform: translateX(-100px); }
        100% { opacity: 1; transform: translateX(0); }    
    }
    li {
        animation: appearing 1s ease-in-out forwards;
    }
</style>

