<template>
  <h1 class="textoCentralizado">Alertas: Exibindo? {{ exibindoAlerta }}</h1>
  <v-alert
    v-if="exibindoAlerta"
    color="error"
    title="Alerta"
    closable
    text="Texto de Alerta"
    icon="mdi-home"
  ></v-alert>
  <v-btn color="info" @click="exibirAlerta()">Exibir | Oculta Alerta</v-btn>
</template>
<script setup>
import { ref } from 'vue';
    const exibindoAlerta = ref(true)
    function exibirAlerta(){
        exibindoAlerta.value = !exibindoAlerta.value
    }
</script>
<style></style>
