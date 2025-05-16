<template>
    <div class="container">
        <label for="id_nombre">Nombre: </label>
        <input v-model="nuevoNombre" id="id_nombre" type="text" />

        <label for="id_apellido">Apellido: </label>
        <input v-model="nuevoApellido" id="id_apellido" type="text" />

        <label for="id_edad">Edad: </label>
        <input v-model="nuevoEdad" id="id_edad" type="number" />

        <label for="id_FechaNacimiento">Fecha de nacimiento: </label>
        <input v-model="nuevoFechaNacimiento" id="id_FechaNacimiento" type="date">

        <label for="id_email">Email: </label>
        <input v-model="nuevoEmail" id="id_email" type="email">

        <button v-on:click=" agregarEstudiante()">Agregar Estudiante</button>

        <ul>
            <li v-for="{ nombre, apellido, edad, fechaNacimiento, email } in lista" :key="nombre">Nombre: {{ nombre }} -
                Apellido: {{ apellido }} - Edad: {{ edad }} - Fecha de nacimiento: {{ fechaNacimiento }} - Email: {{
                email }}</li>

        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            nuevoNombre: "Nuevo",
            nuevoApellido: "Nuevo",
            nuevoEdad: null,
            nuevoFechaNacimiento: null,
            nuevoEmail: null,
            lista: [{ nombre: "Gabriela", apellido: "Rodriguez", edad: 25, fechaNacimiento: "1999-06-29", email: "gabyr@uce.edu.ec" },
            { nombre: "Daniel", apellido: "Torres", edad: 23, fechaNacimiento: "2002-01-10", email: "danit@uce.edu.ec" },
            { nombre: "Carlos", apellido: "Lopez", edad: 28, fechaNacimiento: "1996-04-27", email: "carlols@uce.edu.ec" },
            { nombre: "Steven", apellido: "Cruz", edad: 22, fechaNacimiento: "2003-11-11", email: "stevenc@uce.edu.ec" },
            { nombre: "Belen", apellido: "Castillo", edad: 21, fechaNacimiento: "2004-07-05", email: "belenc@uce.edu.ec" },
            { nombre: "Juan", apellido: "Teran", edad: 20, fechaNacimiento: "2005-12-12", email: "juant@uce.edu.ec" },
            { nombre: "Luis", apellido: "Boada", edad: 19, fechaNacimiento: "2006-10-15", email: "luisb@uce.edu.ec" }
            ]
        };
    },
    methods: {
        agregarEstudiante() {
            const nuevo = {
                nombre: this.nuevoNombre,
                apellido: this.nuevoApellido,
                edad: this.nuevoEdad,
                fechaNacimiento: this.nuevoFechaNacimiento,
                email: this.nuevoEmail
            }
            /*this.lista.unshift(nuevo);*/
            this.lista.push(nuevo);
        },
    }

};
</script>

<style></style>
