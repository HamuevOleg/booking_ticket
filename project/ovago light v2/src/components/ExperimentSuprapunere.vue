<script setup>

</script>

<template>
  <div class="containerul"></div>
  <div class="primul"></div>
  <div class="al_doilea"></div>

</template>

<style scoped>
.containerul {
  display: flex;
  width: 100px;
  flex-direction: column;
  align-items: center;
  /* gap: -60px; */
}

.primul {
  height: 100px;
  align-self: stretch;
  background: #D9D9D9;
}

.al_doilea {
  margin-top: -60px;
  height: 100px;
  align-self: stretch;
  background: #8D3333;
}
</style>
