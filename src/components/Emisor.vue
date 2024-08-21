<script setup>
import { ref } from 'vue';

const mensaje = ref('Datos Personales');
const nombre = ref('');
const apellido = ref('');
const email = ref('');

function enviarFormulario() {
  const datos = {
    nombre: nombre.value,
    apellido: apellido.value,
    email: email.value
  };
  emit('enviar-formulario', datos);
}
</script>

<template>
    <div>
        <h1>{{ mensaje }}</h1>
        <form @submit.prevent="enviarFormulario">
            <label for="nombre">Nombre:</label>
            <input type="text" id="nombre" v-model="nombre"/>

            <label for="apellido">Apellido:</label>
            <input type="text" id="apellido" v-model="apellido"/>

            <label for="email">Email:</label>
            <input type="email" id="email" v-model="email"/>

            <button type="submit">Enviar</button>
        </form>
    </div>
</template>