<script setup>


</script>

<template>

    <svg width="1000" height="1000">
      <path id="motionPath" d="M10,80 C40,10 65,10 95,80 S150,150 180,80" fill="none" stroke="gray"/>

      <circle r="5" fill="red">
        <animateMotion dur="8s" repeatCount="indefinite">
          <mpath href="#motionPath" />
        </animateMotion>
      </circle>

      <path  d="M7.4937 19.8689L5.99457 19.8689L8.49312 11.8735L2.99631 11.3738L0.997467 14.3721H-0.00195312L0.997467 10.3744L-0.0019527 6.3767L0.997468 6.3767L2.99631 9.37496L8.49312 8.87525L5.99457 0.879883H7.4937L12.4908 8.87525H15.4891C16.3186 8.87525 20.4862 9.06264 20.4862 10.3744C20.4862 11.6861 16.3186 11.8735 15.4891 11.8735H12.4908L7.4937 19.8689Z" fill="black"/>

    </svg>


</template>

<style scoped>



</style>
