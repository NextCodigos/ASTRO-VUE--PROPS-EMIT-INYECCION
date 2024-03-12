<template>
    <div>
        <h1>Padre:</h1>
        <!-- El padre envía al hijo estos dos valores -->
        <HijoVue :nombre="nombre" :edad="edad" @modificar="cambiarValor" />
    </div>

    <div>
        <h1>HijoVue:</h1>
        <h2>Te llamas {{ nombre }} y tienes {{ edad }} años</h2>
        <button @click="enviar">Cambiar Valores</button>
    </div>
</template>

<script setup>
import { defineEmits, defineProps, ref } from 'vue';

// Padre




// Hijo
const cambiarValor = (valor1, valor2) => {
    nombre.value = valor1;
    edad.value = valor2;
};

const nombre = ref('JAB');
const edad = ref(20);

const emit = defineEmits(['modificar']);
const enviar = () => {
    emit('modificar', nombre.value, edad.value);
};

const props = defineProps({
    nombre: String,
    edad: Number,
});
</script>

<style></style>