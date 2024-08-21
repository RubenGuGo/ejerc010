<script>
export default {
    data(){
        return {
            mensaje: 'Datos Personales',
            nombre: '',
            apellido: '',
            email: ''
        };
    },
    methods: {
        enviarFormulario(){
            this.$emit('enviar-formulario', {
                nombre: this.nombre,
                apellido: this.apellido,
                email: this.email
            });
        }
    }
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
  color: white;
}

form {
  display: flex;
  flex-direction: column;
}

label {
  margin-top: 10px;
  font-weight: bold;
}

input {
  padding: 8px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  margin-top: 20px;
  padding: 10px;
  border: none;
  border-radius: 5px;
  background-color: #007bff;
  color: white;
  font-size: 16px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
</style>