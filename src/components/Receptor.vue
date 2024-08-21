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
    <h1>Datos</h1>
    <div>
      <p><strong>Nombre:</strong> {{ data.nombre }}</p>
      <p><strong>Apellido:</strong> {{ data.apellido }}</p>
      <p><strong>Email:</strong> {{ data.email }}</p>
    </div>
  </template>

  
<style scoped>
.form-container {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  background-color: #f9f9f9;
}

h1 {
  text-align: center;
  color: black
}

div {
  display: flex;
  flex-direction: column;
}

p {
  padding: 5px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 5px;
  margin-top: 38px;
  font-weight: bold;
}

</style>