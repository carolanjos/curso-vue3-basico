<template>
    <ul>
        <li v-for="nome in nomes">{{ nome }}</li>
    </ul>
</template>

<script setup>
    const nomes = ['Alice', 'Caio', 'Carol', 'David', 'Ana'];
</script>