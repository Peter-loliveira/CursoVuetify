<template>
    <h1>CheckBoxes | Comboboxes:</h1>
    <v-checkbox v-for="item in lista" :label='item.cor' :value='item.cor' :color="item.codigo" v-model="selectedColors"></v-checkbox>
    <v-text-field v-model = 'selectedColors' class="metade">
        <!-- <h3>{{ selectedColors }}</h3> -->
    </v-text-field>
    <br>
    
    <v-combobox class="metade" label="Escolha um pais - Um de Cada Vez" 
    :items="['Brasil', 'Uruguai', 'Argentina', 'Alemanha']">
    </v-combobox>
    
    <v-combobox class="metade" label="Escolha um pais - Vários ao mesmo tempo" 
    :items='listaPaises' multiple v-model="paisSelecionado">
    </v-combobox>
    <h3>Paises selecionado: {{ paisSelecionado }}</h3>

    
</template>
<script setup>
import { ref } from 'vue';

    const lista = ref([
        {cor:'Azul', codigo:'blue'},
        {cor:'Vermelho', codigo:'red'},
        {cor:'Verde', codigo:'green'},
        {cor:'Amarelo', codigo:'yellow'},
        {cor:'Rosa', codigo:'pink'},
    ])
    
    const selectedColors = ref([])
    
    const listaPaises = ref(['Brasil', 'Uruguai', 'Argentina', 'Alemanhaaaaa'])
    const paisSelecionado = ref([])
    
    const alertar = () => alert('TESTE')
</script>
<style>
    
</style>