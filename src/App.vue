<script setup>
import ListagemLivros from '@/components/ListagemLivros.vue'
import MeuCarrinho from '@/components/MeuCarrinho.vue'
</script>

<template>
  <main>
  
  <div class="container-geral">
    <listagem-livros />
    <meu-carrinho />
  </div>
</main>
</template>

<style scoped>
.container-geral {
  display: grid;
  grid-template-columns: 3fr 1fr;
  
}
</style>
