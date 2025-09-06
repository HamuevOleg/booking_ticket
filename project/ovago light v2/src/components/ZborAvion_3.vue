<script setup>

</script>

<template>

  <div class="container_avion animatie_opacitate">
    <!-- <svg class="avion_1" xmlns="http://www.w3.org/2000/svg" width="25" height="23" viewBox="0 0 25 23" fill="none">
      <path d="M9.45236 22.2309L7.69626 22.2309L10.6231 12.9677L4.18407 12.3888L1.84261 15.8625H0.671875L1.84261 11.2309L0.671875 6.59932L1.84261 6.59932L4.18407 10.073L10.6231 9.49405L7.69626 0.230896L9.45236 0.230896L15.306 9.49405L18.8182 9.49405C19.7899 9.49405 24.6719 9.71116 24.6719 11.2309C24.6719 12.7506 19.7899 12.9677 18.8182 12.9677L15.306 12.9677L9.45236 22.2309Z" fill="#FFFFFF"/>
    </svg> -->

    <svg class="avion_1" xmlns="http://www.w3.org/2000/svg" width="31" height="29" viewBox="0 0 31 29" >
      <path class="avion_1_culoare" d="M11.6475 28.2309L9.45236 28.2309L13.1109 16.4414L5.06212 15.7046L2.13529 20.1256H0.671875L2.13529 14.2309L0.671876 8.33616L2.13529 8.33616L5.06212 12.7572L13.1109 12.0204L9.45236 0.230896L11.6475 0.230896L18.9646 12.0204H23.3548C24.5694 12.0204 30.6719 12.2967 30.6719 14.2309C30.6719 16.1651 24.5694 16.4414 23.3548 16.4414H18.9646L11.6475 28.2309Z" />
    </svg>
  </div>



  <!-- <svg class="traseul_1 animatie_opacitate" xmlns="http://www.w3.org/2000/svg" width="1052" height="466" viewBox="0 0 1052 466" fill="none">
    <path class="path_eu" d="M1 164C138 -69 594 -117.5 1051 465.5" stroke="url(#paint0_linear_233_4226)"/>
    <defs>
      <linearGradient id="paint0_linear_233_4226" x1="27" y1="138.5" x2="575" y2="66.9522" gradientUnits="userSpaceOnUse">
        <stop stop-color="#816EFC" stop-opacity="0"/>
        <stop offset="0.995324" stop-color="#FFFFFF"/>
      </linearGradient>
    </defs>
  </svg> -->


</template>

<style scoped>

  .path_eu {
    stroke-dasharray: 1260;
    stroke-dashoffset: 1260;
    animation: dash 24s infinite linear;
  }

  @keyframes dash {
    to {
      stroke-dashoffset: 0;
    }
  }

  .container_avion{
    position: relative;
  }

  .avion_1 {
    position: absolute;
    offset-path: path("M1 205.501C41 151.001 192.5 -9.00627 517.5 1.49316C889.806 13.5209 986 252.501 1006.5 294.501");
    offset-rotate: auto;
    animation: move 24s infinite linear;
    z-index: 5;
  }

  .avion_1_culoare {
    /* animation: schimb 24s infinite linear; */
    fill: #816EFC;
  }

  /* @keyframes schimb {
    0% { fill: #816EFC;}
    36% { fill: rgb(255, 255, 255); }
    90% { fill: rgb(255, 255, 255); }
    100% { fill: rgb(255, 255, 255); }
  } */

  @keyframes move {
    0% { offset-distance: 0%; }
    100% { offset-distance: 100%; }
  }

  .animatie_opacitate{
    animation: fadeIn 24s infinite linear;
  }

  @keyframes fadeIn {
    0% { opacity: 0; }
    18% { opacity: 1; }
    90% { opacity: 1; }
    100% { opacity: 0; }
  }

  
</style>