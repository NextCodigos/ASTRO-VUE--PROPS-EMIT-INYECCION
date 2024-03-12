<template>
    <div>
        <h1>HijoVue:</h1>
        <h2>{{nombre}} y tienes {{edad}} años</h2>
    </div>
</template>

<script setup>
const props = defineProps({
    nombre: String,
    edad: Number,
})
</script>
