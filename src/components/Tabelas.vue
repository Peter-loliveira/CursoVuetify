<template>
  <h1>Tabelas:</h1>
  <div class="bordaTabela">

  
  <v-table theme="light" density="compact" height="200px">
    <thead>
      <tr>
        <th>
          <v-icon icon="mdi-account"></v-icon>
          Nome
        </th>
        <th>
          <v-icon icon="mdi-email"></v-icon>
          Email
        </th>
        <th>Ações</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="contato in listaContatos">
        <td>{{ contato.nome }}</td>
        <td>{{ contato.email }}</td>
        <td class="espacamentoAcoes">
          <v-icon icon="mdi-delete" color="error" @click="alert_()"></v-icon>
          <v-icon
            icon="mdi-file-document-edit"
            color="info"
            @click="edit_()"
          ></v-icon>
          <v-icon
            icon="mdi-content-save"
            color="success"
            @click="save_()"
          ></v-icon>
        </td>
      </tr>
    </tbody>
  </v-table>
</div>
  <br />
  <v-row>
    <v-col>
      <v-text-field label="Nome"></v-text-field>
    </v-col>
    <v-col>
      <v-text-field label="E-mail"></v-text-field>
    </v-col>
    <v-col>
      <v-btn @click="addContact()" color="info">Adcionar</v-btn>
    </v-col>
  </v-row>
  
</template>
<script setup>
import { ref } from "vue";

const alert_ = () => alert("TESTE DE ALERTA!");
const  save_ =() =>  alert("TESTE DE Salvamento!");
const  edit_ = () => alert("TESTE DE Edição!");


const listaContatos = ref([
  { nome: "Peter", email: "peter@email" },
  { nome: "lange", email: "lange@email" },
  { nome: "Oliveira", email: "Oliveira@email" },
  { nome: "Bruno", email: "bruno@email" },
  { nome: "Raymar", email: "raymar@email" },
  { nome: "Jutta", email: "jutta@email" },
  { nome: "Pedro", email: "pedro@email" },
  { nome: "Tairon", email: "tairom@email" },
  { nome: "Malheiros", email: "malheiros@email" },
  { nome: "Cris", email: "cris@email" },
  { nome: "Danubia", email: "danubia@email" },
]);
function addContact() {
  listaContatos.value.push({
    nome: "Adicionado",
    email: "adiconado@email.com",
  });
}
</script>
<style>
.espacamentoAcoes {
  width: 150px;
  display: flex;
  justify-content: space-between;
}
.bordaTabela {
  border: 1px solid black !important;
  width: 60%;
}
</style>
