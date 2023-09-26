<template>
    <h1>CheckBoxes:</h1>
    <v-checkbox v-for="item in lista" :label='item.cor' :value='item.cor' :color="item.codigo" v-model="selectedColors"></v-checkbox>
    <v-text-field v-model = 'selectedColors' >
        <!-- <h3>{{ selectedColors }}</h3> -->
    </v-text-field>
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
</script>
<style></style>