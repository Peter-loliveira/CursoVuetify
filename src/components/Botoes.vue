<template>
  <h1 class="textoCentralizado">Botões:</h1>
  <v-btn color="success">Salvar</v-btn>
  <v-btn color="warning" icon="mdi-cog"></v-btn>
  <v-btn color="info" size="x-small">Tamanho x-small </v-btn>
  <v-btn color="info" size="small">Tamanho small</v-btn>
  <v-btn color="info">Tamanho normal </v-btn>
  <v-btn color="info" size="large">Tamanho large </v-btn>
  <v-btn color="info" size="x-large">Tamanho x-large </v-btn>
  <v-btn color="info" size="x-large">Salvar <v-icon end icon="mdi-check"></v-icon
  ></v-btn>

  <h1>Botões com Funções:</h1>
  <div class="centraizar">
    <v-btn
      color="error"
      @click="subtrair()"
      icon="mdi-minus"
      class="espacoBotoes"
    />
    <h1>{{ valor }}</h1>
    <v-btn
      color="success"
      @click="somar()"
      icon="mdi-plus"
      class="espacoBotoes"
    />
  </div>
</template>
<script setup>
import { ref } from "vue";
const valor = ref(0);
function subtrair() {
  valor.value--;
}
function somar() {
  valor.value++;
}
</script>

<style>
.centraizar {
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
}
h1 {
  margin: 0 10px;
}
</style>
