<script setup>
    import { ref } from 'vue'
    const valor=1;
    const mostrar=ref(true);

    setInterval(() => {
        mostrar.value= !mostrar.value
    }, 500);
</script>

<template>
    <div>
       <p>{{  valor + (Math.floor(Math.random()*10))  }}</p>
       <p> {{ mostrar? 'Se muestra': 'No se Muestra' }}</p>
    </div>
</template>
<style  scoped>

</style>