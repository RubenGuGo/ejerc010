<script setup>
import { ref } from 'vue';
import Receptor from './components/Receptor.vue';
import Formulario from './components/Emisor.vue';

const data = ref({
  nombre: '',
  apellido: '',
  email: ''
});

function actualizarDatos(nuevosDatos) {
  data.value = nuevosDatos;
}
</script>

<template>
  <div class="column" id="Emisor">
    <Formulario @enviar-formulario="actualizarDatos"/>
  </div>
  <div class="column" id="Receptor">
    <Receptor :data="data"/>
  </div>
</template>

<style scoped>
.column {
  display: flex;
  flex-direction: column;
  border: 1px solid black;
}
</style>