<script setup>
import { ref } from 'vue'
import ListagemLivros from '@/components/ListagemLivros.vue'
import MeuCarrinho from '@/components/MeuCarrinho.vue'

const nome = ref('')
const email = ref('')
const senha = ref('')
const rua = ref('')
const bairro = ref('')
const data = ref('')
const senhaConf = ref('')
const enviar = ref(false)
</script>

<template>
  <main>
  
  <div class="container-geral">
    <listagem-livros />
    <meu-carrinho />
  </div>

  <div class="confirmar-compra">
    <form @submit.prevent='enviar = !enviar'>
      <h1>
      Confirmaçao de Compra
    </h1>

    <label for="nome">Nome Completo:</label>

<div><input name="nome" type="text" v-model="nome" placeholder="Digite seu Nome Completo" required /></div>
    </form>
   
    <label for="email">e-Mail:</label>

<div> <input name="email" type="email" v-model="email" placeholder="Digite um E-mail" required /></div>
  </div>
  <label for="senha">Senha:</label>
  <div><input neme="senha" type="password" v-model="senha" placeholder="Digite uma senha" required></div>
  <label for="endereco">Endereço:</label>
<div>
  <input name="endereco" type="text" v-model="rua" placeholder="Digite o Nome da Rua" required><br>
          <input  name="endereco" type="text" v-model="bairro" placeholder="Digite o Nome da Bairro" required><br>
          
</div>
</main>

</template>

<style scoped>
.container-geral {
  display: grid;
  grid-template-columns: 3fr 1fr;
  
}
</style>
