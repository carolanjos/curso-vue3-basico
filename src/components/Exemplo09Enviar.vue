<template>
    <!-- Função para validar o formulário -->
    <form action="www.uol.com.br" @submit="validaFormulario">
        <input type="submit" value="Enviar formulário">
    </form>
</template>

<script setup>
    function validaFormulario(event) {
        alert('Formulário enviado com sucesso');

        event.preventDefault();
    }
    // form tem a tag action que permite um direcionamento para outra página
    // para evitar que o form seja enviado para outra página, é necessário usar o PreventDefault que é uma função que evita o comportamento padrão do form
    // event -> é o evento que está sendo executado e tem o preventDefault que é uma função que evita o comportamento padrão do form
    // só iremos deixar o direcionamento quando todos os dados estiverem corretos e validados
</script>