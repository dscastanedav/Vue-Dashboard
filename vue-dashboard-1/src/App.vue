
<template>
 
 
  <headerrr>
    <template v-slot:slot1>
      <img class=" bg-white-500 p-4 m-2 gap-1" src="./assets/HeaderImages/Trazado1820.png">
    </template> 
    <template v-slot:slot2>
      <img class="bg-white-500 p-4 m-2 gap-1" src="./assets/HeaderImages/Grupo1528.png">      
    </template>
    <template v-slot:slot3 >
      <div class="flex items-center border rounded border-r-slate-300 hover:border-indigo-300 w-64 h-10 mx-10">
        <img class=" object-scale-down bg-white-500 p-0 m-0 w-128 h-8" src="./assets/HeaderImages/lupa.png">
        <input class=" object-scale-down w-48 h-8 p-4 m-2" placeholder="Búsqueda" >
      </div>
    </template>
    <template v-slot:slot4>
      <img class="bg-white-500 p-4 m-2 gap-1" src="./assets/HeaderImages/Trazado1292.png">
    </template>
    <template v-slot:slot5>
      <h2>Ver Sitio</h2>
    </template>
    <template v-slot:slot6>
       <img class="bg-white-500 p-4 m-2 gap-1" src="./assets/HeaderImages/Trazado911.png">
    </template>
    <template v-slot:slot7>
      <img class="bg-white-500 p-4 m-2 gap-1" src="./assets/HeaderImages/christopher-campbell-28567-unsplash.png">
    </template>
    <template v-slot:slot8>
      <div class="flex-col">
        <h2 class="font-semibold">Andrés Suarez</h2>
        <h2>Administrador</h2>
      </div>
    </template>
    <template v-slot:slot9>
      <img class="bg-white-500 p-4 m-2 gap-1 mx-5" src="./assets/HeaderImages/Trazado914.png">
    </template>

  </headerrr>

  

</template>

<script>
/* eslint-disable vue/no-unused-components */

import headerrr from './components/headerrr.vue'
 
export default {
  name: 'App',
  components: {
    headerrr
  }
}
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
#wrapper {
  max-width: 940px;
  margin: 0 auto;
  padding: 0 5%;
  clear: both;
}
</style>
