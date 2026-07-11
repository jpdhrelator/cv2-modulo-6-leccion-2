
<script>
export default{

    data(){
        return {
            titulo:'Hola',
            contador:0

        }

    },
    methods:{
       incrementar() {
         this.contador++  // ← this
        } 
    }
}

</script>
<template>
    <h1>Options</h1>
    <h3>Titulo: {{ titulo }}</h3>
    <p>{{ contador }}</p>

    <button @click="incrementar">Incrementar</button>
</template>