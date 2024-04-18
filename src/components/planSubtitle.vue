<template>
  <h2 class="subtitle">{{ subtitle }}</h2>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps(['subtitle']);
</script>
