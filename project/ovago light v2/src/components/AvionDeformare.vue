<script setup>
  
</script>

<template>

  <div class="obiectul_parinte">

    <svg class="stil_avion" xmlns="http://www.w3.org/2000/svg" width="250" height="234" viewBox="0 0 250 234" fill="none">
      <path d="M91.4634 234L73.1707 234L103.659 135.474L36.5854 129.316L12.1951 166.263H0L12.1951 117L5.19396e-06 67.7368L12.1951 67.7368L36.5854 104.684L103.659 98.5263L73.1707 0L91.4634 0L152.439 98.5263H189.024C199.146 98.5263 250 100.836 250 117C250 133.164 199.146 135.474 189.024 135.474H152.439L91.4634 234Z" fill="#816EFC"/>
    </svg>

  </div>

  <svg xmlns="http://www.w3.org/2000/svg" width="250" height="234" viewBox="0 0 250 234" fill="none">
    <path d="M91.4634 234L73.1707 234L103.659 135.474L36.5854 129.316L12.1951 166.263H0L12.1951 117L5.19396e-06 67.7368L12.1951 67.7368L36.5854 104.684L103.659 98.5263L73.1707 0L91.4634 0L152.439 98.5263H189.024C199.146 98.5263 250 100.836 250 117C250 133.164 199.146 135.474 189.024 135.474H152.439L91.4634 234Z" fill="#816EFC"/>
  </svg>



</template>

<style scoped>
  .obiectul_parinte{
    perspective: 600px;
    perspective-origin: 30% 50%;
    margin: 364px;
  }

  .stil_avion{
    transform: rotateX(10deg) rotateY(10deg) rotateZ(10deg); /* Will look 3D because of perspective skew(15deg, 15deg) */
    transform-style: preserve-3d;
  }

</style>
