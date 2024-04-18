<template>
  <header>
    <div>
      <span id="logo">Liquid Gold Box</span>
      <img src="./assets/logo.png" alt="logo">
    </div>
  </header>

  <div class="content">
    <Title :title="pageTitle" />
    <Subtitle :subtitle="pageSubtitle" />
    <plan-picker :plans="plan" />
  </div>
</template>

<script setup>
import planPicker from './components/plan-picker.vue';
import Title from './components/planTitle.vue';
import Subtitle from './components/planSubtitle.vue';

</script>

<style scoped>
header {
  line-height: 1.5;
}
 
.logo {
  display: block;
  margin: 0 auto 2rem;
}
 
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }
 
  .logo {
    margin: 0 2rem 0 0;
  }
 
  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>