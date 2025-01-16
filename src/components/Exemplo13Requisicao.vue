<template>
    <h1>Requisições</h1>
    <table>
        <tr v-for="v in vetor">
            <td>{{ v.userId }}</td>
            <td>{{ v.id }}</td>
            <td>{{ v.title }}</td>
            <td>{{ v.body }}</td>
        </tr>
    </table>
</template>

<script setup>
// usando api falsas
// posts - 100 postagens com algumas caracteristicas

// vetor contendo as postagens
import { onMounted, ref } from 'vue';

let vetor = ref([]);

onMounted(() => {
    fetch('https://jsonplaceholder.typicode.com/posts') //api falsa
    .then(retorno => retorno.json()) // esse trecho faz a requisição e retorna um json
    .then(retorno => vetor.value = retorno) // esse trecho pega o retorno e atribui ao vetor
});
</script>