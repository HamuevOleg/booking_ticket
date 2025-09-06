<script setup>

import ZborAvion_3 from './ZborAvion_3.vue';

</script>

<template>

  <div class="spatiul_gol">
    <div class="to_be">
      to be continued ...
    </div>

    <ZborAvion_3 class="avion_zbor"/>
  </div>

</template>

<style scoped>
  .spatiul_gol{
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100vh;
    justify-content: center;
    align-items: center;
    position: relative;
  }

  .to_be{
    color: #000;
    font-family: jost;
    font-size: 48px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
  }

  .avion_zbor{
    position: absolute;
    width: 1048px;
    top: 30%;
    left: 50%;

    transform: translate(-50%, -50%);


  }

</style>