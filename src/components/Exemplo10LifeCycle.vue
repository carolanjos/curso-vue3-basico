<template>
    <h1>{{ texto }}</h1>
</template>

<script setup>
    import { onMounted, ref } from 'vue';

    let texto = ref('Hello World!');
    // vai exibir o valor do texto e 3 segundos depois o texto vai ser alterado
    // lifecycle é quando o componente já foi montado e está pronto para ser exibido

    // onMounted -> é uma função que é executada quando o componente é montado
    onMounted(() => {
        setTimeout(() => {
            texto.value = 'Alterando texto!';
            }, 3000);
    });
</script>