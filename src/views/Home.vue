<template>
  <AlertasView />
  <div class="separador"></div>
  <Botoes />
  <div class="separador"></div>
  <Breadcrumbs />
  <div class="separador"></div>
</template>

<script setup>
import AlertasView from '@/components/Alertas.vue';
import Botoes from '@/components/Botoes.vue';
import Breadcrumbs from '@/components/Breadcrumbs.vue';

</script>
<style>
.separador{
  margin: 5px 0;
  height: 2px;
  background-color: #555;
}
</style>