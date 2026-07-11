<script setup>
    import { ref } from 'vue'
    const id = ref(42)
    const colorAttr = ref('#42b883')
    const img="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRm_iBN45BNZwAsPGIigPElN0MaKTw7ixckb6JLH5fXjmP98LBGJTceH1Q&s=10";
    const caricatura="jugador";

</script>

<template>
    <div v-bind:id="`caja-${id}`">El Div tiene el id caja-{{ id }}</div>
    <div v-bind:style="{color:colorAttr}">Texto cualquiera</div>
    <img   width="200px" src="https://i.pinimg.com/736x/a6/b7/6c/a6b76c27fee5b4336ec4dc9d3b510217.jpg" alt="caricatura"/>
    <img   width="200px" v-bind:src="img" v-bind:alt="caricatura"/>
</template>
<style  scoped>

</style>