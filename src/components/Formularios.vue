<template>
  <h1>Foemularios:</h1>
  <v-row>
    <v-col>
      <v-text-field
        type="text"
        label="Digite seu Nome"
        v-model="nome"
      ></v-text-field>
    </v-col>
    <v-col>
      <v-text-field
        type="number"
        label="Digite um nr"
        v-model="idade"
      ></v-text-field>
    </v-col>
  </v-row>
  <v-text-field>
    <h3>Seu nome é {{ nome }}, e você tem {{ idade }} anos.</h3>
  </v-text-field>
</template>
<script setup>
import { ref } from "vue";

const nome = ref("Peter");
const idade = ref(0);

</script>
<style></style>
