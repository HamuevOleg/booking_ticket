<script setup>

</script>

<template>

  <div class="avion_1">
    <svg xmlns="http://www.w3.org/2000/svg" width="25" height="23" viewBox="0 0 25 23" fill="none">
      <path d="M9.45236 22.2309L7.69626 22.2309L10.6231 12.9677L4.18407 12.3888L1.84261 15.8625H0.671875L1.84261 11.2309L0.671875 6.59932L1.84261 6.59932L4.18407 10.073L10.6231 9.49405L7.69626 0.230896L9.45236 0.230896L15.306 9.49405L18.8182 9.49405C19.7899 9.49405 24.6719 9.71116 24.6719 11.2309C24.6719 12.7506 19.7899 12.9677 18.8182 12.9677L15.306 12.9677L9.45236 22.2309Z" fill="#816EFC"/>
    </svg>
  </div>

  <svg class="traseul_1" xmlns="http://www.w3.org/2000/svg" width="1052" height="466" viewBox="0 0 1052 466" fill="none">
    <path class="path_eu" d="M1 164C138 -69 594 -117.5 1051 465.5" stroke="url(#paint0_linear_233_4226)"/>
    <defs>
      <linearGradient id="paint0_linear_233_4226" x1="27" y1="138.5" x2="575" y2="66.9522" gradientUnits="userSpaceOnUse">
        <stop stop-color="#816EFC" stop-opacity="0"/>
        <stop offset="0.995324" stop-color="#816EFC"/>
      </linearGradient>
    </defs>
  </svg>

  <!-- <div class="avion_2">
    <svg xmlns="http://www.w3.org/2000/svg" width="25" height="23" viewBox="0 0 25 23" fill="none">
      <path d="M9.45236 22.2309L7.69626 22.2309L10.6231 12.9677L4.18407 12.3888L1.84261 15.8625H0.671875L1.84261 11.2309L0.671875 6.59932L1.84261 6.59932L4.18407 10.073L10.6231 9.49405L7.69626 0.230896L9.45236 0.230896L15.306 9.49405L18.8182 9.49405C19.7899 9.49405 24.6719 9.71116 24.6719 11.2309C24.6719 12.7506 19.7899 12.9677 18.8182 12.9677L15.306 12.9677L9.45236 22.2309Z" fill="#816EFC"/>
    </svg>
  </div> -->




</template>

<style scoped>

  /* .traseul_1{
    position: absolute;
    top: 92%;
    left: 48%;
    transform: translate(-50%, -50%);
  } */
    .path_eu {
      stroke-dasharray: 1260;
      stroke-dashoffset: 1260;
      animation: dash 24s infinite linear, fadeIn 4s forwards ease-in;
    }

    @keyframes dash {
      to {
        stroke-dashoffset: 0;
      }
    }

  .avion_1 {
    position: absolute;
    top: 10px;
    /* left: 20%;
    transform: translate(-50%, -50%); */
    offset-path: path("M1 164C138 -69 594 -117.5 1051 465.5");
    offset-rotate: auto;
    animation: move 24s infinite linear, fadeIn 3s forwards ease-in;
    opacity: 0; /* start off as invisible */
  }

  .avion_2 {
    position: absolute;
    top: 70%;
    right: 90%;
    transform: translate(-50%, -50%);
    offset-path: path("M1453.99 211.968C1351.63 2.69456 1074.61 -48.8817 761.319 49.314C369.709 172.059 81.0529 405.477 1 737.976");
    offset-rotate: auto;
    animation: move 32s infinite linear, fadeIn 3s forwards ease-in;
    opacity: 0; /* start off as invisible */
    animation-delay: 2s; 
  }

  @keyframes move {
    0% { offset-distance: 0%; }
    100% { offset-distance: 100%; }
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

</style>