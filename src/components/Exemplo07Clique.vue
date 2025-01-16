<template>
    <button @click="mensagem">Clique aqui</button>
</template>

<script setup>
    function mensagem() {
        alert('Trabalhando com eventos de clique');
    }
</script>