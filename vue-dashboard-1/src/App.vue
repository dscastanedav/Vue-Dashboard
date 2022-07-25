
<template>
 <div class="bg-slate-200 ">
 
  <headerrr class="bg-white">
    <template v-slot:slot1>
      <img class=" bg-white-500 p-4 m-2 gap-1" src="./assets/HeaderImages/Trazado1820.png">
    </template> 
    <template v-slot:slot2>
      <img class="bg-white-500 p-4 m-2 gap-1" src="./assets/HeaderImages/Grupo1528.png">      
    </template>
    <template v-slot:slot3 >
      <div class="flex items-center border rounded border-r-slate-300 hover:border-indigo-300 w-64 h-10 mx-20">
        <img class=" object-scale-down bg-white-500 p-0 m-0 w-128 h-8" src="./assets/HeaderImages/lupa.png">
        <input class=" object-scale-down w-48 h-8 p-4 m-2" placeholder="Búsqueda" >
      </div>
    </template>
    <template v-slot:slot4>
      <img class="bg-white-500 p-4 m-2 gap-1" src="./assets/HeaderImages/Trazado1292.png">
    </template>
    <template v-slot:slot5>
     <h2 class="text-base">Ver Sitio</h2>
    </template>    
    <template v-slot:slot6>
       <img class="bg-white-500 p-4 m-2 gap-1" src="./assets/HeaderImages/Trazado911.png">
    </template>
    <template v-slot:slot7>
      <img class="bg-white-500 p-4 m-2 gap-1 ml-20" src="./assets/HeaderImages/christopher-campbell-28567-unsplash.png">
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

  
  <dashboarddd class="bg-white">
    <template v-slot:slot1>
      <img class=" bg-white-500 p-4 m-2 gap-1 border-2 rounded border-slate-50 shadow-md	" 
      src="./assets/DashboardImages/NoPathcopia(8).png">
    </template>
    <template v-slot:slot2>
      <div class="flex-col text-left">
        <h2 class="font-semibold">Del campo Express</h2>
        <h2 class="text-sm"> Url de mi tienda en línea</h2>
        <h2 class="text-sm text-cyan-600">https://delcampoexpress.viveshops.co</h2>
      </div>
    </template>
    <template v-slot:slot3>
      <img class="bg-white-500 mx-2 mt-10 w-128 h-5 " src="./assets/DashboardImages/filecopy.png">
    </template>
    
  <template v-slot:slot4>
    <div class="grid grid-cols-6 grid-rows-5 items-center ml-5 -mt-8 text-sm text'left
    border border-transparent border-l-slate-200">
      <h2 class="-ml-12  font-semibold col-span-3 row-span-1">Completa tu cuenta (2/8)</h2>
      <div class="w-full -ml-10 bg-gray-200 rounded-full h-2.5 dark:bg-gray-700 col-span-3 row-span-1" >
        <div class="bg-blue-600 h-2.5 rounded-full " style="width: 25%"></div>
      </div>


<img class="bg-white-500 mt-6 ml-12 w-128 h-4  col-span-1" src="./assets/DashboardImages/Trazado1232.png">
  <h2 class=" mt-6 -ml-7 mr-3 col-span-1 text-left" >Crear Producto</h2>
<img class="bg-white-500 mt-6 ml-7 w-128 h-4 col-span-1 invisible" src="./assets/DashboardImages/Trazado1235.png">

<img class="bg-white-500 mt-5 ml-12 w-128 h-4  col-span-1" src="./assets/DashboardImages/Trazado1233.png">
  <h2 class=" mt-5 -ml-7 col-span-1 text-slate-400" >Definir logo y colores</h2>
<img class="bg-white-500 mt-5 ml-8 w-128 h-4 col-span-1" src="./assets/DashboardImages/Trazado1235.png">

<img class="bg-white-500 mt-1 ml-12 w-128 h-4  col-span-1" src="./assets/DashboardImages/Grupo1826.png">
  <h2 class=" mt-1 -ml-7 col-span-2 text-left " >Definir cobertura envíos</h2>

<img class="bg-white-500 mt-1 ml-12 w-128 h-4  col-span-1" src="./assets/DashboardImages/Trazado1236.png">
  <h2 class=" mt-1 -ml-7 col-span-1 text-slate-400">Personalizar plantilla</h2>
<img class="bg-white-500 mt-1 ml-8 w-128 h-4 col-span-1" src="./assets/DashboardImages/Trazado1235.png">

<img class="bg-white-500 -mt-4 ml-12 w-128 h-4  col-span-1" src="./assets/DashboardImages/Trazado1238.png">
  <h2 class=" -mt-4 -ml-7 col-span-2 text-left ">Agregar método de pago</h2>
  
<img class="bg-white-500 -mt-4 ml-12 w-128 h-4  col-span-1" src="./assets/DashboardImages/megaphone.png">
  <h2 class=" -mt-4 -ml-7 col-span-2 text-left ">Activar campañas</h2>

  <img class="bg-white-500 -mt-9 ml-12 w-128 h-4  col-span-1" src="./assets/DashboardImages/Trazado1239.png">
  <h2 class=" -mt-9 -ml-7 col-span-2 text-left ">Establecer dominio</h2>

  <img class="bg-white-500 -mt-9 ml-12 w-128 h-4  col-span-1" src="./assets/DashboardImages/Trazado1138.png">
  <h2 class=" -mt-9 -ml-7 col-span-2 text-left ">Completar documentos</h2>

    </div>
    
  </template>

  <template v-slot:slot5>
      <!-- <h2 class="border border-black col-span-1" >Crear Producto</h2>
      <img class="bg-white-500  w-128 h-5 border border-black col-span-1" src="./assets/DashboardImages/Trazado1235.png">
       -->

    
  </template>





  </dashboarddd>


  
</div>
</template>

<script>
/* eslint-disable vue/no-unused-components */

import headerrr from './components/headerrr.vue'
import dashboarddd from './components/dashboarddd.vue'


 
export default {
  name: 'App',
  components: {
    headerrr,
    dashboarddd,
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
