<script setup>

  document.addEventListener("DOMContentLoaded", () => {
    const path = document.getElementById("motionPath");
    const arrow = document.getElementById("arrow");
    const pathLength = path.getTotalLength();

    let progress = 0;
    const speed = 0.001;

    function animate() {
      progress += speed;
      if (progress > 1) progress = 0;

      const currentPoint = path.getPointAtLength(progress * pathLength);
      const nextPoint = path.getPointAtLength((progress + 0.001) * pathLength);

      const dx = nextPoint.x - currentPoint.x;
      const dy = nextPoint.y - currentPoint.y;
      const angle = Math.atan2(dy, dx) * (180 / Math.PI);

      arrow.setAttribute("transform", `translate(${currentPoint.x}, ${currentPoint.y}) rotate(${angle})`);

      requestAnimationFrame(animate);
    }

    animate();
  });
  
</script>

<template>

  <svg width="600" height="400" viewBox="0 0 600 400">
    <!-- The path to follow -->
    <path id="motionPath" d="M50,300 C150,100 450,100 550,300" stroke="#fff" fill="none"/>

    <!-- Arrow shape (a triangle here, but could be an image too) -->
    <!-- <polygon id="arrow" points="-10,-5 10,0 -10,5" fill="red" /> -->
  <path id="arrow" d="M7.4937 19.8689L5.99457 19.8689L8.49312 11.8735L2.99631 11.3738L0.997467 14.3721H-0.00195312L0.997467 10.3744L-0.0019527 6.3767L0.997468 6.3767L2.99631 9.37496L8.49312 8.87525L5.99457 0.879883H7.4937L12.4908 8.87525H15.4891C16.3186 8.87525 20.4862 9.06264 20.4862 10.3744C20.4862 11.6861 16.3186 11.8735 15.4891 11.8735H12.4908L7.4937 19.8689Z" fill="black"/>

  </svg>

</template>

<style scoped>

</style>
