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
            <input type="text" id="nombre" v-model="name"/>

            <label for="apellido">Apellido:</label>
            <input type="text" id="apellido" v-model="apellido"/>

            <label for="email">Email:</label>
            <input type="email" id="email" v-model="email"/>

            <button type="submit">Enviar</button>
        </form>
    </div>
</template>