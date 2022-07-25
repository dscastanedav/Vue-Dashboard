<template>
    <div class="flex border borde-slate-300 items-center m-10 p-8 shadow-md">
        <div id="div1">
            <slot name="slot1"></slot>
        </div>
        <div id="div2">
            <slot name="slot2"></slot>
        </div>
        <div id="div3">
            <slot name="slot3"></slot>
        </div>
        <div id="div4">
            <slot name="slot4"></slot>
        </div>
        <div id="div5">
            <slot name="slot5"></slot>
        </div>
      
       
    </div>
</template>

<script>
    export default {
        name:'mis-statistics'
        
    }
</script>

<style scoped>

</style>