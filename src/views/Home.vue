<template>
  <Formularios />
  <div class="separador"></div>
  <Grids />
  <div class="separador"></div>
  <Layouts />
  <div class="separador"></div>
  <Listas />
  <div class="separador"></div>
  <Tabelas />
  <div class="separador"></div>
  <Chips />
  <div class="separador"></div>
  <AlertasView />
  <div class="separador"></div>
  <Botoes />
  <div class="separador"></div>
  <Breadcrumbs />
  <div class="separador"></div>
  <Cardes />
  <div class="separador"></div>
  <Icones />
  <div class="separador"></div>
</template>

<script setup>
import AlertasView from '@/components/Alertas.vue';
import Botoes from '@/components/Botoes.vue';
import Breadcrumbs from '@/components/Breadcrumbs.vue';
import Cardes from '@/components/Cardes.vue';
import Icones from '@/components/Icones.vue';
import Chips from '@/components/Chips.vue';
import Tabelas from '@/components/Tabelas.vue';
import Listas from '@/components/Listas.vue';
import Layouts from '@/components/Layouts.vue';
import Grids from '@/components/Grids.vue';
import Formularios from '@/components/Formularios.vue';

</script>
<style>
.separador{
  margin: 5px 0;
  height: 2px;
  background-color: #555;
}
</style>