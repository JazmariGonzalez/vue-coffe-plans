<template>
    <div class="plan">
         <div class="description">
           <span class="title">  
             {{ name }}
           </span>
         </div>
       </div>
  </template>
  
  <script setup>
  //Macro es una funcion especialidad en vue que me permite crear defineProps (que ya las importa), no se tiene que intregrar porque Vue ya lo hace, para agregar  nombre propiedades siempre usar camelcassing
  defineProps(['name']);
  
  </script>