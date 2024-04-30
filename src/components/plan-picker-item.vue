<template>
    <div 
    @click="select"
    :class="{'select-plan':isSelected}" 
    class="plan">
         <div class="description">
           <span class="title">  
             {{ name }}
           </span>
         </div>
       </div>
  </template>

  <script setup>
  import { computed } from 'vue';
  //Creando un evento
  const emit = defineEmits(['select']);
  const props = defineProps({
    name: {
      type: String,
      required: true,
    },
    selectedPlan: {
    type:String
  },
  });

  const select = () => {
    //Detonando el evento
    emit('select', props.name);
  }
//Creando propiedad computada
const isSelected = computed(() => {
  return props.name == props.selectedPlan;
});

  </script>
  <style scoped>
  .select-plan {
    background-color:#7afad4;
}
</style>