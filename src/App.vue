<script setup>
import { reactive } from 'vue';

const movie = reactive({
    id: 1,
    title: 'Star Wars',
    year: 1977,
    director: 'George Lucas',
    actors: ['Mark Hamill', 'Harrison Ford', 'Carrie Fisher'],
    duration: 121,
});

</script>

<template>
    <dl>
        <!-- la balise template ne sera pas rendue dans le DOM, elle sert juste pour la directive v-for -->
        <template v-for="(item, key) in movie" :key>
            <dt>{{ key }}</dt>
            <dd>{{ item }}</dd>
        </template>
    </dl>
</template>

<style scoped>

</style>

