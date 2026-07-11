<script setup>
import { ref } from 'vue'

const nuevaTarea= ref('');
const tareas=ref([
    {id:1,texto:'Aprender Templates',hecha:true},
    {id:2,texto:'Dominar v-for',hecha:false},
]);

function agregarTarea() {
    if(!nuevaTarea.value.trim()) return;
    const id=tareas.value.length+1;
    tareas.value.push({id, texto:nuevaTarea.value, hecha:false});
    nuevaTarea.value='';
}
function toogleHecha(tarea) {
    tarea.hecha = !tarea.hecha;
}
function eliminarTarea(id) {
    tareas.value= tareas.value.filter(t => t.id !==id);
}

</script>

<template>
    <form @submit.prevent="agregarTarea" >
        <input v-model.trim="nuevaTarea" type="text" placeholder="Nueva Tarea..."/>
        <button>Agregar Tarea</button>
    </form>

    <p v-if="tareas.length ===0">No hay tareas aún 🎉</p>
    <ul v-else>
        <li v-for="tarea in tareas" :key="tarea.id">
            <span @click="toogleHecha(tarea)"> {{ tarea.texto }}</span>
            
            <button @click="eliminarTarea(tarea.id)">✕</button>
            <br>
            <small>{{ (tarea.hecha?'Lista':'Pendiente') }}</small>
        </li>
    </ul>
</template>