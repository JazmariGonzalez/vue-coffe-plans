<script setup>
import FancyButton from './components/FancyButton.vue'
</script>
 
<template>
<FancyButton> 
    <template v-slot:icon ="slotprops"> 
         {{ slotprops.hover ? '🚀': '❌'}} 
    </template> 
    <template v-slot:default> 
    <strong style="text-decoration: underline;">E</strong>nviar 
</template> 
</FancyButton>
<FancyButton> 
    <template v-slot:icon = "{ hover }"> 
     {{ hover  ? '❌': '🚀'}} 
    </template> 
    <template v-slot:default> 
    <strong style="text-decoration: underline;">C</strong>ancelar
</template> 
</FancyButton>
</template>
 
<style scoped>
</style>