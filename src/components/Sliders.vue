<template>
  <h1>Sliders</h1>
  <v-slider
    :min="0"
    :max="5000"
    class="metade"
    color="error"
    v-model="valorSlider"
    :step="10"
    :prepend-icon='iconeVolume'
    thumb-label
    thumb-size="20"
    thumb-color="red"
  ></v-slider>
  <v-slider
    direction="vertical"
    :min="0"
    :max="5000"
    class="metade"
    color="success"
    v-model="valorSlider"
    :step="10"
    :prepend-icon='iconeVolume'
    thumb-label
    thumb-size="20"
    thumb-color="green"
  ></v-slider>
  <h3>Valor do Slider é de: {{ valorSlider }}</h3>
  <h4>{{ iconeVolume }}</h4>
</template>
<script setup>
import { ref } from "vue";

const valorSlider = ref(0);

const iconeVolume = ref('mdi-volume-low')

// if(valorSlider == 0){
//     iconeVolume = 'mdi-volume-mute'
// } else{
//     if(valorSlider == 50){
//         iconeVolume = 'mdi-volume-high'
//     }
// }
</script>
<style></style>
