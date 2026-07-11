<script setup>
    import { ref } from 'vue'
    const botonDeshabilitado = ref(true)

    setInterval(() => {
        botonDeshabilitado.value=!botonDeshabilitado.value;
    }, 1000);

</script>

<template>
    <button :disabled="botonDeshabilitado" type="button">Boton cualquiera</button>
 </template>