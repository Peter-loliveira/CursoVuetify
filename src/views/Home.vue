<template>
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

</script>
<style>
.separador{
  margin: 5px 0;
  height: 2px;
  background-color: #555;
}
</style>