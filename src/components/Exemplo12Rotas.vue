<template>
    <a href="#/">Página 1</a>
    |
    <a href="#/pagina2">Página 2</a>
    <!-- Exibiçao das páginas -->
     <component :is="currentView" />
</template>

<script setup>
import { ref, computed } from 'vue';
import Pagina1 from './Pagina1.vue';
import Pagina2 from './Pagina2.vue';
import PaginaErro from './PaginaErro.vue';

// criar uma estrutura de rotas -> contendo o caminho e o componente
const routes = {
    '/': Pagina1,
    '/pagina2': Pagina2,
    '/404': PaginaErro
}

// obter o contéudo a partir da cerquila ex: http://localhost:8080/#/sobre o retorno será: #/sobre
const referenciaRota = ref(window.location.hash);

// executa a ação quando realizar a navegação entre páginas. Obter o contéudo a partir da cerquilha
window.addEventListener('hashchange', () => { // isso é um evento que é disparado quando a cerquilha é alterada
    referenciaRota.value = window.location.hash; // obter o valor da cerquilha da URL 
    // usa hash pq é uma forma de navegação que não recarrega a página
});

// função responsavel por exibir a pagina especifica
const currentView = computed(() => {
    return routes[referenciaRota.value.slice(1) || '/'] || PaginaErro
})

</script>