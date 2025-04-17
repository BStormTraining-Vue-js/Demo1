<script setup>
import { reactive, computed } from 'vue';
const products = reactive([{name: 'Eau 50cl', quantity: 2, price: 0.9}, {name: 'Soda 33cl', quantity: 3, price: 0.7}]);
// création d'un state calculé pour le prix total
const total = computed(() => products.reduce((prev, current) => prev + current.quantity * current.price, 0).toFixed(2));
</script>

<template>
    <!-- ici le prix total est recalculé à chaque rendu -->
    <p>Prix total: {{ products.reduce((prev, current) => prev + current.quantity * current.price, 0).toFixed(2) }}€</p>
    <!-- utilisation du state calculé -->
    <p>Prix total: {{ total }}€</p>
</template>

<style scoped>
</style>

