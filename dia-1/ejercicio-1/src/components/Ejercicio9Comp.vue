<script setup>
import { ref } from 'vue'
import CompCualquiera from './CompCualquiera.vue';


const frutas = ref([
    { id: 1, nombre: 'Manzana' },
    { id: 2, nombre: 'Pera' },
    { id: 3, nombre: 'Plátano' }
]);
const usuario = ref({ 
    nombre: 'Ana', 
    edad: 25, 
    ciudad: 'Santiago' 
})
function agregar() {
    const newId = frutas.value.length + 1;
    frutas.value.push({ id: newId, nombre: `Otra ${newId}` });
}
</script>

<template>

    <button @click="agregar" type="button">Agregar</button>

    <ul>
        <li v-for="(fruta, index) in frutas" :key="fruta.id">
            {{ index }} {{ fruta.nombre }}
        </li>
    </ul>

    <CompCualquiera v-for="(fruta, index) in frutas" :key="fruta.id" />


    <ul>
        <li v-for="(valor, propiedad) in usuario">
            {{ propiedad }} --> {{ valor }}
        </li>
    </ul>
</template>