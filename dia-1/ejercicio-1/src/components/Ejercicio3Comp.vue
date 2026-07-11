<script setup>
    import { ref } from 'vue'
    const msg = ref('Escribí algo...');
    const textoHtml=`
        <p><b>Soy un texto </b> para renderizar</p>    
    `;
    setInterval(()=>{
        msg.value= 'Escribí algo...'+Math.floor((Math.random()*100));
    },1000);

</script>

<template>
    <div>
        
        <p v-once>Congelado con v-once: {{ msg }}</p>
        <p>{{ msg }}</p>

        <div> renderizado com texto plano{{ textoHtml }}</div>
        <div v-html="textoHtml"></div>

    </div>
</template>
<style  scoped>

</style>