<template>
    <!-- Obter props -->
    <p>Nome: {{ nome }}</p>
    <p>Idade: {{ idade }}</p>
    <p>Cidade: {{ cidade }}</p>

    <ul>
        <li v-for="v of vetor">{{ v }}</li>
    </ul>

    <button @click="funcao">Clique aqui</button>
</template>

<script setup>
    import Exemplo11Props1 from './Exemplo11Props1.vue';
    const props = defineProps(['nome', 'idade', 'cidade', 'vetor', 'funcao']);

    //props é um objeto que contém todas as propriedades passadas para o componente
    //defineProps é uma função que recebe um array com o nome das propriedades que o componente deve receber
    //esses props vem do Exemplo11Props1.vue
</script>
