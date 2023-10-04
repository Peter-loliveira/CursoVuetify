<template>
  <h1>Formularios mais avançados</h1>
  <v-card class="mx-auto" max-width="600"  title="Crie sua Conta">
    <v-container>
      <v-text-field
        label="Digite seu Nome"
        type="text"
        v-model="dados.nome"
      ></v-text-field>
      <v-text-field
        label="Digite seu Email"
        type="email"
        v-model="dados.email"
      ></v-text-field>
      <v-text-field
        label="Digite sua Senha"
        type="password"
        v-model="dados.password"
      ></v-text-field>
      <v-select label="Escolha seu Pais" :items='paises' v-model='dados.pais'></v-select>
      <v-card-actions>
        <v-btn color="success" @click = 'salvar()'>Salvar</v-btn>
        <v-btn color="error">Cancelar</v-btn>
      </v-card-actions>
      <h1>{{dados.nome}} </h1>
      <h1>{{ dados.email }}</h1>
      <h1>{{ dados.pais }}</h1>
      <h1>{{ dados.password }}</h1>
      <br>
    </v-container>
  </v-card>
</template>
<script setup>
import { ref } from "vue";

const dados = ref({});
const paises = [
  "Alemanha",
  "Argentina",
  "Brasil",
  "Uruguai",
  "EUA",
  "França",
  "China",
  "Jápão",
];

const salvar = ()=> alert(`Dados salvos com sucesso!`)
</script>
<style></style>
