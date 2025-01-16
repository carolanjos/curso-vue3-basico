<!-- HTML -->
<template>
    <p>{{ 'Olá ' + nome + ', você tem ' + idade + ' anos. ' }}</p>
    <p>{{ numero1+numero2 }}</p>
</template>
  
<!-- SCRIPT -->
<script setup>
    // variaveis
    let nome = 'Alice';
    let idade = 32;
    let numero1 = 20;
    let numero2 = 25;
</script>