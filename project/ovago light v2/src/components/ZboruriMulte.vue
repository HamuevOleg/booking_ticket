<script setup>

  import ZborAvion from './ZborAvion_1.vue';

</script>


<template>

  <div class="positionare_avion">
  <ZborAvion/>
  <ZborAvion/>
  </div>


</template>

<style scoped>
  .positionare_avion{
    position: absolute;
    top: 114%;
    left: 50%;
    transform: translate(-50%, -50%);
  
  }

</style>