<template>
    <div class="plan">
         <div class="description">
           <span class="title">  
             {{ name }} 👍 Likes: {{ likes }} 
           </span>
         </div>
       </div>
  </template>
  
  <script setup>
  defineProps({
    name: {
      type: String,
      required: true,
      //default: "Plan sin nombre",
    }, 
    likes: {
      type: Number,
      default: 0,
    }
  });
  </script>