<template>
    <div ref="plansWrapper"
    class="plans">
      <plan-picker-item  
      @select="printSelected"
      :selectedPlan="selectedPlan"
      v-for="plan in plans" 
      :name="plan"
      v-bind:key="plan" />
      <p style="font-size: 30px;"> Counter: {{ counter }}</p> 
    </div>
</template>

<script setup>
import { ref, onMounted , onUpdated} from 'vue';
import planPickerItem from './plan-picker-item.vue';
const plans = ref ([ 
  "El soltero", 
  "El adicto", 
  "El viajero", 
  ]);
const plansWrapper = ref(null);

const selectedPlan = ref(null);

const printSelected  = (payload) => {
  selectedPlan.value = payload;
  }
  //Creando una referencia reactivas 
const counter = ref(0);
//Creando un metodo para incrementar el contador 
const processId = setInterval(() => {
  console.log('Incremento contador');
  counter.value++;
}, 1000);
  //Regristando en CB (Call Back (FUNCION QUE SE EJECUTA)) onMonunted 
  onMounted (() => {
 //Obteniendo la referencia del elemento .plans 
  console.log(plansWrapper.value);
  });
  onUpdated (() => {
  console.log('Componente Plans Picker desmontando')
  clearInterval(processId);
  });
</script>