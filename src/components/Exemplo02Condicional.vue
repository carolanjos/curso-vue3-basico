<template>
    <h1 v-if="exibir">Hello World</h1>

    <p v-if="media >= 7">Aprovado(a)</p>
    <p v-else-if="media >= 5">Em exame</p>
    <p v-else>Reprovado(a)</p>
</template>

<script setup>
// diretiva são funcionalidades para tags
// v-if é uma diretiva que exibe ou não um elemento
// se v-if for true, o elemento é exibido
// se v-if for false, o elemento não é exibido
    let exibir = true;
    let media = 4;

</script>