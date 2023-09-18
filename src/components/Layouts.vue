<template>
  <h1>Layouts:</h1>
  <div class="bordas">
    <v-card>
      <v-layout>
        <v-app-bar title="Minha Aplicação 1 - Titulo do Menu na parte superior">
          <v-btn
            start
            color="primary"
            @click="showMenu1()"
            icon="mdi-menu"
          ></v-btn>
        </v-app-bar>
        <v-navigation-drawer v-model="menuOn1">
          <v-list>
            <v-list-item title="Opção de Menu 01"></v-list-item>
            <v-list-item title="Opção de Menu 02"></v-list-item>
          </v-list>
        </v-navigation-drawer>
        <v-main style="min-height: 200px"> </v-main>
      </v-layout>
    </v-card>
  </div>
  <div class="bordas">
    <v-card>
      <v-layout>
        <v-app-bar title="Minha Aplicação - 2 - Segunda barra de menus">
        </v-app-bar>
        <v-navigation-drawer v-model="menuOn2">
          <v-list>
            <v-list-item title="Menu Esquerda 01"></v-list-item>
            <v-list-item title="Menu Esquerda 02"></v-list-item>
          </v-list>
        </v-navigation-drawer>
        <v-main style="min-height: 200px">
          <div class="ConteudoEspacado">
            <v-btn
              start
              color="primary"
              @click="showMenu2()"
              icon="mdi-menu"
            ></v-btn>
            Conteudo
            <v-btn
              start
              color="primary"
              @click="showMenu3()"
              icon="mdi-menu"
            ></v-btn>
          </div>
        </v-main>
        <v-navigation-drawer location="right" v-model="menuOn3">
          <v-list>
            <v-list-item title="Menu Direita 01"></v-list-item>
            <v-list-item title="Menu Direita 02"></v-list-item>
          </v-list>
        </v-navigation-drawer>
      </v-layout>
    </v-card>
  </div>
  <div class="bordas">
    <v-card>
      <v-layout>
        <v-navigation-drawer>
          <v-list>
            <v-list-item title="Opção de Menu 01"></v-list-item>
            <v-list-item title="Opção de Menu 02"></v-list-item>
          </v-list>
        </v-navigation-drawer>
        <v-app-bar title="Minha Aplicação 3 - Titulo na parte do Conteudo">
        </v-app-bar>
        <v-main style="min-height: 200px">Conteudo</v-main>
      </v-layout>
    </v-card>
  </div>
</template>

<script setup>
import { ref } from "vue";
const menuOn1 = ref(null);
const menuOn2 = ref(null);
const menuOn3 = ref(null);
const showMenu1 = () => (menuOn1.value = !menuOn1.value);
const showMenu2 = () => (menuOn2.value = !menuOn2.value);
const showMenu3 = () => (menuOn3.value = !menuOn3.value);
</script>

<style>
.bordas {
  border: 1px solid black;
  margin-bottom: 5px;
}
.ConteudoEspacado {
  display: inline;
  justify-content: space-between;
}
</style>
