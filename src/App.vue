<script setup>
import Receptor from './components/Receptor.vue';
import Formulario from './components/Emisor.vue'
</script>

<template>
  <div class="column" id="Emisor">
    <Formulario/>
  </div>
  <div class="column" id="Receptor">
    <Receptor/>
  </div>
</template>

<style scoped>
.column {
  display: flex;
  flex-direction: column;
  border: 1px solid black;
}
</style>