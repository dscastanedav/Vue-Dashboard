<template>
    <div class="modal-overlay" v-show="open">
    <div class="modal-content">
      <div>
      <slot></slot>




      <br>
      <button class="font-semibold  " @click="$emit('close')">Close</button>
      <!--No funciono items end-->
    </div>
  </div>
  </div>
</template>

<script>


    export default {
        name: 'mi-popup',
 
        props:{
         open:{
          type:Boolean,
          required:true
         }
        }
    }

</script>

<style scoped>
.modal-overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: grid;
  justify-content: center;
  align-items: center;
  background-color: rgba(0, 0, 0, 0.3);
}

.modal-content {
  /*font-family: "Fondamento", cursive;*/
  padding: 20px;
  background: #fff;
  border-radius: 2px;
  display: inline-block;
  min-height: 800px;
  margin: 1rem;
  position: relative;
  min-width: 500px;
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
  justify-self: center;
}
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1; 
}
 
/* Handle */
::-webkit-scrollbar-thumb {
  background: #888; 
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #555; 
}

</style>







