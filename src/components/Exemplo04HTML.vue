<template>
    <!-- v-html  -->
    <div v-html="texto"></div>
    <div v-html="textoMostrandoDiferença"></div>
    <!-- interpolação de texto -->
    {{ textoMostrandoDiferença }}
</template>

<script setup>
// v-html responsavel por criar dinamicamente um conteudo html
    let texto = "Aprendendo a diretiva v-html"; 
    let textoMostrandoDiferença = '<p style="color: red;">Aprendendo a diretiva v-html</p>'; 
// interpolacao de texto faz a mesma coisa mas a diferença é que o v-html renderiza o html, 
// então não é somente texto, mas toda a estrutura html
</script>