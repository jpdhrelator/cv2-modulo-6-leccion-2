<script setup>
    import { ref } from 'vue'
    let titulo=ref("titulos");
    const saludo="Holas"

    function mayus() {
        titulo.value= titulo.value.toUpperCase();
    }
    function minus() {
        titulo.value= titulo.value.toLowerCase();
    }
</script>

<template>
    <div>
        <h1>{{ titulo }}</h1>
        <small>{{ saludo }}</small>
        

        <button @click="mayus" type="button">Mayus</button>
        <button @click="minus" type="button">Minus</button>
    </div>
</template>
<style  scoped>

</style>