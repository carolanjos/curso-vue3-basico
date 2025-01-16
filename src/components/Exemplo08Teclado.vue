<template>
    <input type="text" @keyup="mensagem">
    <br>
    <br>
    <input type="text" @keyup.enter="mensagem">
    <!-- nesse acima, só vai aparecer a mensagem depois que o usuario clica no enter -->
    <br>
    <br>
    <input type="text" @keyup.r="mensagem">
    <!-- nesse acima, só vai aparecer a mensagem depois que o usuario clica no "r" -->
</template>

<script setup>
    function mensagem() {
        alert('Executando a função');
    }
</script>