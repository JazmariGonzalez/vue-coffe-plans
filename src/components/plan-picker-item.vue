<template>
    <div  @click="select" 
    :class="{'select-plan':selected}" 
    class="plan">
         <div class="description">
           <span class="title">  
             {{ name }} {{ selected ? '✔': ''}} 
           </span>
         </div>
       </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  const selected = ref(false)
  const select = () => {
    selected.value  = true
  }
  defineProps({
    name: {
      type: String,
      required: true,
      //default: "Plan sin nombre",
    }
  });
  </script>
  <style scoped>
  .select-plan {
    background-color:#7afad4;
}
</style>