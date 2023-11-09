<script setup>
import ContainerView from './ContainerView.vue';
import Card from './components/Card.vue';
import HeaderView from './HeaderView.vue'
</script>

<template>
  <div clas="container contain">
    <div class="row mt-4 justify-content-center">
      <HeaderView />
        <Card msg="Vite + Vue" />
    </div>
  </div>
  
</template>

<style scoped>
</style>
