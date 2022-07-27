
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




<!-- para texto
        required size="10"
           placeholder="Username"
           minlength="4" maxlength="8" -->

           <!-- step="10" min="0" max="100" -->

        <!--Aqui va el popup-->     <!--POPUP-->     <!--POPUP-->       <!--POPUP-->


          <button @click="isOpen = true" class=" mt-6 -ml-7 mr-3 col-span-1 text-left" >Crear Producto</button>
          <!-- <teleport to="#modal-root"> -->
            <popup :open="isOpen" @close="isOpen=!isOpen">
           
              <div class="text-left">
                <h2 class="text-xl font-bold text-center">Crear producto</h2>
                <br>
                <h2 class="text-lg	font-semibold">Informacion del producto</h2>
                <br>

                <form @submit="submitForm">   <!--INICIO FORM-->
                <div class="flex flex-col">
                  <label for="descripcion" class="">Descripcion</label>
                  <select id="categoria" class="border rounded border-slate-300 h-15 text-slate-400">
                    <option value="">Seleccione una categoria</option>
                    <option value="alimentos">Alimentos</option>
                    <option value="tecnologia">Tecnologia</option>
                    <option value="vestimenta">Vestimenta</option>
                  </select>
                </div>

                <br>
                <div class="flex flex-col">
                  <label for="titulo" class="">Titulo</label>
                  <input type="text" id="titulo" class="border rounded border-slate-300 h-15" v-model="formValues.titulo" required maxlength="40">
                </div>
                <br>
                <div class="flex flex-col">
                  <label for="descripcion" class="">Descripcion</label>
                  <input type="text" id="descripcion" class="border rounded border-slate-300 h-15" v-model="formValues.descripcion" maxlength="100">
                </div>
                <br>
                <div class="flex flex-col">
                  <label for="descripcionPro" class="">Descripcion pro</label>
                  <textarea type="text" id="descripcionPro" class="border rounded border-slate-300 h-15" v-model="formValues.descripcionPro" maxlength="1000"></textarea>
                </div>
                <br>
                <h2>Variantes</h2>      <!--VARIANTES SELECTORES-->
                <br>
                <div class="grid grid-cols-2 border border-transparent border-b-slate-400">
                  <label for="talla" class="">Talla</label>
                  <select id="talla" v-model="formValues.talla"><!--como espaciar flex items y que funcione-->
                    <option value=""> </option>
                    <option value="s">S</option>
                    <option value="m">M</option>
                    <option value="l">L</option>
                  </select>
                </div>
                <br>
                <div class="grid grid-cols-2 grid grid-cols-2 border border-transparent border-b-slate-400">
                  <label for="color" class="">Color</label>
                  <select id="color" v-model="formValues.color"><!--como espaciar flex items y que funcione-->
                    <option value=""></option>
                    <option value="rojo">Rojo</option>
                    <option value="amarillo">Amarillo</option>
                    <option value="verde">Verde</option>
                    <option value="azul">Azul</option>
                  </select>
                </div>
                <br>
                <div class="grid grid-cols-2 grid grid-cols-2 border border-transparent border-b-slate-400">
                  <label for="sabor" class="">Sabor</label>
                  <select id="sabor" v-model="formValues.sabor"><!--como espaciar flex items y que funcione-->
                    <option value=""></option>
                    <option value="dulce">Dulce</option>
                    <option value="salado">Salado</option>
                    <option value="acido">Acido</option>
                  </select>
                </div>
              
                <div class="flex flex-row items-center ml-20">
                   <img class="bg-white-500 p-6  mx-0 h-13" src="./assets/PopupImages/mas.png">
                  <h2 class="text-sky-400	">Agregar grupo de Toppings</h2>
                </div>
                
                <h2 class="text-lg	font-semibold">Precio y disponibilidad</h2>
                <br>

                <div class="flex flex-row">
                  <div class="flex flex-col">
                    <label for="cantidad" class="">Cantidad</label>
                    <input type="text" v-model="formValues.cantidad" id="cantidad" class="border rounded border-slate-300 h-15 mr-2 my-0.5  gap-4" 
                    required step="1" min="0" max="1000000" onkeypress="if ( isNaN( String.fromCharCode(event.keyCode) )) return false;">
                  </div>
                  <div class="flex flex-col">
                    <label for="sku" class="">SKU</label>
                    <input type="text" v-model="formValues.sku" id="sku" class="border rounded border-slate-300 h-15 mr-2 my-0.5  gap-4" 
                    required maxlength="20" onkeypress="if ( isNaN( String.fromCharCode(event.keyCode) )) return false;">
                  </div>
                </div>

                <div class="flex flex-row">
                  <div class="flex flex-col">
                    <label for="moneda" class="">Moneda</label>
                    <select id="moneda" v-model="formValues.moneda" class="border rounded border-slate-300 h-19 text-slate-400 mr-9 my-0.5 " ><!--como espaciar flex items y que funcione-->
                    <option value="">Seleccione moneda</option>
                    <option value="peso">Pesos Colombianos</option>
                    <option value="dolar">Dolares</option>
                    <option value="euro">Euros</option>
                  </select>
                  </div>
                  <div class="flex flex-col">
                    <label for="precio" class="">Precio</label>
                    <input type="text" v-model="formValues.precio" id="precio" class="border rounded border-slate-300 h-15  mr-2 my-0.5  gap-4" 
                    required step="50" min="0" max="1000000000" onkeypress="if ( isNaN( String.fromCharCode(event.keyCode) )) return false;">
                  </div>
                </div>
                <br>
                <h2 class="text-lg	font-semibold">Precio y disponibilidad</h2>

                <div class="flex flex-row">
                  

                  <div class="flex flex-col">
                    <h2 class="semibold">Peso</h2>
                    <div class="flex flex-row">
                      <input type="text" v-model="formValues.peso" id="peso" class="border rounded border-slate-300 h-15 my-0.5 mr-2 gap-4" 
                      required step="1" min="0" max="10000000" onkeypress="if ( isNaN( String.fromCharCode(event.keyCode) )) return false;">
                      <h2 class="mx-1">Grs</h2>
                    </div>
                    
                  </div>

                  <div class="flex flex-col">
                    <h2 class="semibold">Alto</h2>
                    <div class="flex flex-row">
                       <input type="text" v-model="formValues.alto" id="alto" class="border rounded border-slate-300 h-15 my-0.5 mr-2 gap-4" 
                       step="10" min="0" max="1000000" onkeypress="if ( isNaN( String.fromCharCode(event.keyCode) )) return false;">
                    <h2 class="mx-1">cm</h2>
                    </div>
                  </div>

                  <div class="flex flex-col">
                     <h2 class="semibold">Ancho</h2>
                     <div class="flex flex-row">
                      <input type="text" v-model="formValues.ancho" id="ancho" class="border rounded border-slate-300 h-15 my-0.5 mr-2 gap-4" 
                      required step="10" min="0" max="1000000" onkeypress="if ( isNaN( String.fromCharCode(event.keyCode) )) return false;">
                    <h2 class="mx-1">cm</h2>
                    </div>
                  </div>

                  <div class="flex flex-col">
                    <h2 class="semibold">Profundo</h2>
                    <div class="flex flex-row">
                      <input type="text" v-model="formValues.profundo" id="profundo" class="border rounded border-slate-300 h-15 my-0.5 mr-2 gap-4" 
                      required step="10" min="0" max="1000000" onkeypress="if ( isNaN( String.fromCharCode(event.keyCode) )) return false;">
                     <h2 class="mx-1">cm</h2>  
                    </div>
                  </div>
                  <br>
                </div>
                <br>
                 <h2 class="text-lg	font-semibold">Fotos del producto</h2>
                  <h2 class="ml-10"> <b>Importante: </b>Las imagenes son el componente mas importante de <br>
                  un buen e-commerce. Por favor cargue imagenes de buena calidad <br>y tamaño. Le recomendamos usar estandares de 
                  proporcion 4:3 y <br>color de fondo unificado
                  </h2>  
                  <br>
                  <label for="avatar">Escoja una imagen: </label>

                <div class="grid grid-cols-2 items-left">
                  <input type="file"
                    id="avatar" name="avatar"
                    accept="image/png, image/jpeg">
                  <button class="font-semibold border rounded border-slate-300 p-2 bg-sky-500 w-20 text-white" >Submit</button>
                </div>
                  

                </form><!--FIN FORM-->

              </div>
            </popup>
          <!-- </teleport> -->









          
        <img class="bg-white-500 mt-6 ml-7 w-128 h-4 col-span-1 invisible" src="./assets/DashboardImages/Trazado1235.png">

        <img class="bg-white-500 mt-5 ml-12 w-128 h-4  col-span-1" src="./assets/DashboardImages/Trazado1233.png">
          <h2 class=" mt-5 -ml-7 col-span-1 text-slate-400">Definir logo y colores</h2>
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
  </dashboarddd>

  <statistics class="bg-white">
    
    <template v-slot:slot1>
      <div class="grid grid-rows-2 grid-cols-4">
        <h2 class="font-bold text-lg text-left col-span-3 row-span-1">Estadísticas</h2>

         <div class="border-2 rounded border-slate-60 shadow-md text-sm p-0.5 mx-8 col-span-1 row-span-1 justify-end items-end">
          <select id="tiempo" v-model="fechas">
            <option value="">Seleccionar fecha</option>
            <option value="ultimos 7 dias">Últimos 7 días</option>
            <option value="ultimo mes">Último mes</option>
            <option value="ultimo year">Último año</option>
          </select>

        </div>
      </div>
    </template>
    
    
  </statistics>



  


  
 </div>
</template>

<script>
/* eslint-disable vue/no-unused-components */

import headerrr from './components/headerrr.vue'
import dashboarddd from './components/dashboarddd.vue'
import popup from "./components/popup.vue";
import statistics from "./components/statistics.vue";
import {ref} from "vue";
 
export default {
  name: 'App',
  components: {
    headerrr,
    dashboarddd,
    popup,
    statistics
  },
  data() {
    return {
      //showModal: false,
      //todas las variables son dinamicas por lo que hay riesgo de informacion enrronea en los formularios
      //por esta razon se usa el tipado, asi se podrian inicializar como constantes vacias de un tipo de dato especifico
      fechas:'',
      formValues:{
        titulo:'',
        descripcion:'',
        descripcionPro:'',
        categoria:'',
        talla:'',
        color:'',
        sabor:'',
        precio:'' ,
        moneda:'' ,
        cantidad:'' ,
        sku:'' ,
        peso:'',
        alto:'',
        ancho:'',
        profundo:'',
      }
    };
  },
  setup(){
    const isOpen = ref(false)
    return {isOpen}
  },
  methods:{
    submitForm(){
      event.preventDefault()
      console.log('Form values', this.formValues)
    }
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
