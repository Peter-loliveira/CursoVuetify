<template>
  <h1>Formularios mais avançados</h1>

  <v-form class="metade" v-model="valido">
    <v-text-field
      :rules='regrasNome'
      type="text"
      label="Digite seu Nome"
      v-model="nome"
    ></v-text-field>
    <v-text-field
      :rules='regrasIdade'
      type="number"
      label="Digite sua idade"
      v-model="idade"
    ></v-text-field>
    <v-text-field
      :rules='regrasEmail'
      type="email"
      label="Digite seu emailç"
      v-model="email"
    ></v-text-field>
  </v-form>

  <v-card class="mx-auto" max-width="600" title="Crie sua Conta">
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
      <v-select
        label="Escolha seu Pais"
        :items="paises"
        v-model="dados.pais"
      ></v-select>
      <v-card-actions>
        <v-btn color="success" @click="salvar()">Salvar</v-btn>
        <v-btn color="error">Cancelar</v-btn>
      </v-card-actions>
      <h1>{{ dados.nome }}</h1>
      <h1>{{ dados.email }}</h1>
      <h1>{{ dados.pais }}</h1>
      <h1>{{ dados.password }}</h1>
      <br />
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
const salvar = () => alert(`Dados salvos com sucesso!`);

const nome = ref("");
const valido = ref(false);
const regrasNome = [
    value => {
      if(value) {
        return true
      } 
        return 'Campo Obrigatório'
      
    },
    value => {
      if(value.length < 10) {
        return 'Nome muito curto'
      }
        return true
        
    }
]

const idade = ref(0)
const regrasIdade =[
  value =>{
    if(value >= 0 && value <=120) {
      return true
    } return 'Idade Invalida'
  }
]

const email = ref("@")
const regrasEmail = [
  value => {
    if(/.+@.+\.+/.test(value)){
      return true
    } return 'Email inválido'
  }
]


</script>
<style></style>
