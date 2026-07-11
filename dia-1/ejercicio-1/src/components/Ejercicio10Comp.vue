<script setup>
import { ref } from 'vue'

const nombre= ref('Mariana');
function manejaSubmit() {
    alert(`nombre ingreado--> ${nombre.value}`)
}
</script>

<template>
    <form @submit.prevent="manejaSubmit" action="">
        <input v-model.trim="nombre" name="nombre" type="text" placeholder="Tu Nombre"/>
         <button>Enviar</button>
    </form>
  <br>
    <small>valor de variable-->{{ nombre }} cantidad de caracteres:{{ nombre.length }}</small>
</template>