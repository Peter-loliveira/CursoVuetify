<template>
  <h1>Cards:</h1>
  <v-card
    color="success"
    width="50%"
    prepend-icon="mdi-home"
    title="Curso Vuetify - Card Simples"
    text="Curso de intodução aos componente de Vuetify"
  ></v-card>
  <br />

  <v-card color="warning" width="50%" prepend-icon="mdi-check">
    <template v-slot:title>Curso Vuetify</template>
    <template v-slot:text>
      Usando Templates
      <h3>
        Usando Templates temos mais liberdade, pois podemos usar TAGs HTML
      </h3>
    </template>
  </v-card>
  <br />

  <v-card color="error" width="50%" prepend-icon="mdi-account">
    <v-card-title> Curso Vuetify - Card com TAGs especificas </v-card-title>
    <v-card-text> Usando TAGs </v-card-text>
  </v-card>
  <br />
  <v-card color="info" width="50%">
    <v-img
      class=""
      height="200"
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
      cover
    >
      <v-card-title>Top 10 Australian beaches</v-card-title>
    </v-img>
    <v-card-title> Cards com Botões de Ações </v-card-title>
    <v-card-text>
      Aqui temos a possivilidade com uma TAG de colocar botões para realizar
      ações
    </v-card-text>
    <v-car-actions class="central">
      <v-btn color="success">Ação</v-btn>
      <v-btn color="warning">Cuidado</v-btn>
      <v-btn color="error">Apagar</v-btn>
      <v-btn color="pink">Apagar</v-btn>
    </v-car-actions>
  </v-card>
</template>
<script setup></script>

<style>
.central {
  display: flex;
  justify-content: space-around;
  padding: 10px 0;
}
.align-end{
    display: flex;
    height: 100%;
    width: 100%;
    align-items: center;
}
</style>
