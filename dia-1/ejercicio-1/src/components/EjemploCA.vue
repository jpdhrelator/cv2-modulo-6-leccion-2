
<script setup>
import {ref} from 'vue'; 

    let titulo="Hola 2";
    let contador=ref(0);

    function incrementar(){
        contador.value++;
    }

</script>
<template>
    <h1>Composition API</h1>
    <h3>Titulo: {{ titulo }}</h3>
    <p>{{ contador }}</p>

    <button @click="incrementar">Incrementar</button>
</template>