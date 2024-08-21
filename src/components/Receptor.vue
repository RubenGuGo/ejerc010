  <script setup>
  import { defineProps } from 'vue';
  
  const props = defineProps({
    data: {
      type: Object,
      required: true,
    },
  });
  </script>

<template>
    <div>
      <h2>Datos</h2>
      <p><strong>Nombre:</strong> {{ data.nombre }}</p>
      <p><strong>Apellido:</strong> {{ data.apellido }}</p>
      <p><strong>Email:</strong> {{ data.email }}</p>
    </div>
  </template>

  
  <style scoped>
  p {
    margin: 5px 0;
  }
  </style>