<template>
 
 <h1>Fundación "Mi Casa"</h1>
 <h2>Ficha de Mascotas</h2>
 
 <div>
 <FichaMascotas
 v-if="componenteActivo== `FichaMascotas`"/>
 
 </div>

</template>

<script setup>

import { ref } from 'vue';
import FichaMascotas from './components/FichaMascotas.vue';

const componenteActivo = ref ("FichaMascotas")


  
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

}
</style>
