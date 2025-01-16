<template>
    <p class="ok" v-if="validacao">Validação OK</p>
    <p class="falha" v-else>Validação Falhou</p>
    <p :class="validacao ? 'ok' : 'falha'">Utilizando a diretiva class</p>
    <!-- se validacao for true entao ok mas se for false entao falha (? : - ternário -> se então) -->
    
</template>

<script setup>
    // variavel lógica - quando for verdadeiro: verde == falso: vermelho
    let validacao = true;
</script>

<style scoped>
.ok{color: green;}

.falha{color: red;}
</style>