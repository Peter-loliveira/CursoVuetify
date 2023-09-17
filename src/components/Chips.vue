<template>
  <h1>CHIPS:</h1>
  <v-chip 
    v-for="item in lista"
    :color= 'item.cor'
    class="espacamentoChips"    
    size="large" 
    closable>
    <v-icon start icon="mdi-email"></v-icon>
    {{ item.nome }} {{ item.valor }}
  </v-chip>
</template>
<script setup>
import { ref } from 'vue';
    const lista = ref([
        {nome:'Peter', cor:'blue', valor:0},
        {nome:'Maria', cor:'red', valor:15},
        {nome:'Bruno', cor:'orange', valor:7},
        {nome:'Ray', cor:'green', valor:3},
        {nome:'Ray', cor:'gray', valor:1000},
    ])
</script>
<style>
.espacamentoChips{
    margin-left: 5px;
}
</style>
