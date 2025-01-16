<template>
    <input type="text" v-model="texto" />
    <p>{{ texto }}</p>
    <!-- o ref é capaz de -->
</template>

<script setup>
// tem que importar o ref para ele ser reativo
// o texto fica reativo
import { ref } from 'vue';

// o v-model é responsavel por fazer a ligação entre o input e a variavel
// responsavel por lidar com elementos de formularios, text-area, select, input, etc
    let texto = ref('');
</script>