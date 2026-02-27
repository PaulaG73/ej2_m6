<template>
 
 <h1>Fundación "Mi Casa"</h1>
 <h3>Ficha de Mascotas</h3>
 <nav class="nav-tabs">
<button v-for="comp, index in componentes" :key="index"
@click= "componenteActivo = comp.nombre"
:class= "['nav-btn', {activo: componenteActivo== comp.nombre}]"
>
{{ comp.label }}
</button>

 </nav>
 <div class="contenido">
 <FichaMascotas
 v-if="componenteActivo== `FichaMascotas`"/>
 
 </div>

</template>

<script setup>

import { ref } from 'vue';
import FichaMascotas from './components/FichaMascotas.vue';

const componenteActivo = ref ("FichaMascotas")
const componentes = [
  {nombre: "FichaMascotas", label: "Listar Mascota"}]

  
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
