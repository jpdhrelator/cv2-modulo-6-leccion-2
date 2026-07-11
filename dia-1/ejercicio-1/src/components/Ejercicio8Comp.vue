<script setup>
    import { ref } from 'vue'
 
    const estado = ref('cargando'); // cargando-listo-error
    const meVeo= ref(true);
</script>

<template>

    <button @click="estado='cargando'" type="button"> Cargando</button>
    <button @click="estado='listo'" type="button"> Listo</button>
    <button @click="estado='error'" type="button"> Error</button>
    <button @click="meVeo=!meVeo" type="button"> Toogle Me Veo</button>
   
    <p v-if="estado=='cargando'"> Cargando...</p>
    <p v-else-if="estado=='listo'">Contenido cargado ✅</p>
    <p v-else>Error al cargar ❌ </p>


    <p v-show="meVeo">Me veo</p>

</template>