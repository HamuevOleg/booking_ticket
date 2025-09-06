<script setup>


</script>

<template>
<svg xmlns="http://www.w3.org/2000/svg" width="1052" height="466" viewBox="0 0 1052 466" fill="none">
  <path class="path_eu" d="M1 164C138 -69 594 -117.5 1051 465.5" stroke="url(#paint0_linear_233_4226)"/>
  <defs>
    <linearGradient id="paint0_linear_233_4226" x1="27" y1="138.5" x2="575" y2="66.9522" gradientUnits="userSpaceOnUse">
      <stop stop-color="#816EFC" stop-opacity="0"/>
      <stop offset="0.995324" stop-color="#816EFC"/>
    </linearGradient>
  </defs>
</svg>

</template>

<style scoped>

/* .path_eu {
  stroke-dasharray: 100;
} */

.path_eu {
  stroke-dasharray: 1500;
  stroke-dashoffset: 1500;
  animation: dash 24s linear forwards;
}

@keyframes dash {
  to {
    stroke-dashoffset: 0;
  }
}


</style>
