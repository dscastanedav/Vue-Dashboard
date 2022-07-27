<template>
    <div class="flex border border-transparent border-b-slate-300 items-center -mt-12 shadow-md">
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
        <div id="div6">
            <slot name="slot6"></slot>
        </div>
        <div id="div7">
            <slot name="slot7"></slot>
        </div>
        <div id="div8">
            <slot name="slot8"></slot>
        </div>
        <div id="div9">
            <slot name="slot9"></slot>
        </div>
    </div>
    
</template>

<script>
    export default {
        name: "my-header"
    }
</script>

<style scoped>
  

    

</style>