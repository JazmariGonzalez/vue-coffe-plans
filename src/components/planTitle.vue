<template>
    <h1 class="title"> {{ title }}</h1>
  </template>
  
  <script setup>
  import { defineProps } from 'vue';
  
  const props = defineProps(['title']);
  </script>