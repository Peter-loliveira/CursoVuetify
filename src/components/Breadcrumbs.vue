<template>
  <h1 class="textoCentralizado">breadcrumbs:</h1>
  <v-breadcrumbs :items="listabreadcrumbs">
    <template v-slot:divider>
      <v-icon size="x-small" icon="mdi-chevron-right"></v-icon>
    </template>
  </v-breadcrumbs>
</template>
<script setup>
import { ref } from "vue";
const listabreadcrumbs = ref([
  { title: "Home", href: "/", disabled: false },
  { title: "Noticias", href: "https://www.google.com.br",disabled: false},
  { title: "Videos", href: "https://youtube.com.br",disabled: false },
]);
</script>
<style>
.textoCentralizado {
  text-align: center;
}
</style>
