<template>
    <div class="container">
        <img src="https://ingenioycomunicacion.com/wp-content/uploads/2023/07/placeholder-1.png
        " alt="No se puede cargar">

        <div class="container-2"></div>
        <div class="pregunta-container">
            <input v-model="pregunta" type="text" placeholder="Hazme una pregunta ">
            <p>Recuerda terminar con un signo de pregunta(?)</p>
            <h2>{{ pregunta }}</h2>
            <h1>{{ respuesta }}</h1>
        </div>

    </div>
</template>

<script>
export default {
    data() {
        return {
            pregunta: null,
            respuesta: null
        };
    },
    watch: {
        pregunta(value, oldValue) {
            console.log("Valor actual " + value)
            console.log("Valor anterior " + oldValue)

        }
    },
};
</script>

<style scoped>
.container-2,
img {
    height: 100vh;
    width: 100vw;
    max-height: 100%;
    max-width: 100%;
    position: fixed;
    left: 0px;
    top: 0px;
}

.container-2 {
    background-color: rgba(0, 0, 0, 0.3);
}

.pregunta-container {
    position: relative;
}

input {
    width: 250px;
    padding: 10px 15px;
    border-radius: 5px;
    border: none;
    margin-top: 80px;
}

input:focus {
    outline: none;
}

p {
    color: white;
    font-size: 25px;
}

h1,
h2 {
    color: white;
}

h2 {
    margin-top: 70px;
}
</style>