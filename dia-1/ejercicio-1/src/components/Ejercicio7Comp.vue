<script setup>
    import { ref } from 'vue'
 
    const contador = ref(0);

    function incrementar() {
        contador.value++;
    }
    function decrementar() {
        contador.value--;
    }
</script>

<template>
    <h3>Contador: {{ contador }}</h3>
    <button v-on:click="incrementar" type="button">Aumentar +</button>
    <button @click="decrementar" type="button">Disminuir -</button>
    <button @click="contador=0" type="button">Resetear</button>

</template>