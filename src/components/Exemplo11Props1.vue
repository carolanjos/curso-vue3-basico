<template>
    <Exemplo11Props2 nome="Carol" idade="23" :cidade="cidade" :vetor="cidades" :funcao="mensagem"></Exemplo11Props2>
</template>

<script setup>
    import Exemplo11Props2 from './Exemplo11Props2.vue';
    // props estáticos

    // Variáveis
    let cidade = 'São Paulo';
    // utilizando dois pontos para passar a variável cidade como propriedade -> prop dinamico
    // referenciando cidade
    let cidades = ['São Paulo', 'Rio de Janeiro', 'Belo Horizonte', 'Curitiba'];

    function mensagem() {
        alert('Função criada no componente: Exemplo11Props1');
    };
</script>
