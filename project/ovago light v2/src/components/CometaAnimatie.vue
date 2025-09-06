<script setup>

  document.addEventListener("DOMContentLoaded", () => {
    const path = document.getElementById("motionPath");
    const arrow = document.getElementById("arrow");
    const trailGroup = document.getElementById("trailGroup");
    const pathLength = path.getTotalLength();

    const trail = [];
    const maxTrailLength = 30;
    const speed = 0.002;
    let progress = 0;

    function animate() {
      progress += speed;
      if (progress > 1) progress = 0;

      const point = path.getPointAtLength(progress * pathLength);
      const nextPoint = path.getPointAtLength((progress + 0.001) * pathLength);
      const dx = nextPoint.x - point.x;
      const dy = nextPoint.y - point.y;
      const angle = Math.atan2(dy, dx) * (180 / Math.PI);

      // Update main arrow
      arrow.setAttribute("transform", `translate(${point.x}, ${point.y}) rotate(${angle})`);

      // Add to trail
      trail.push({ x: point.x, y: point.y, angle });

      if (trail.length > maxTrailLength) {
        trail.shift();
      }

      // Clear old trail visuals
      trailGroup.innerHTML = "";

      // Render trail
      trail.forEach((pos, i) => {
        const fade = i / trail.length; // 0 to 1
        const ghost = document.createElementNS("http://www.w3.org/2000/svg", "polygon");
        ghost.setAttribute("points", "-10,-5 10,0 -10,5");
        ghost.setAttribute("fill", `rgba(255, 0, 0, ${fade})`);
        ghost.setAttribute("transform", `translate(${pos.x}, ${pos.y}) rotate(${pos.angle})`);
        trailGroup.appendChild(ghost);
      });

      requestAnimationFrame(animate);
    }

    animate();
  });



</script>

<template>

<svg width="600" height="400" viewBox="0 0 600 400" style="border: 1px solid #ccc">
  <!-- Path -->
  <path id="motionPath" d="M50,300 C150,100 450,100 550,300" stroke="#ccc" fill="none"/>

  <!-- Group to hold the trail -->
  <g id="trailGroup"></g>

  <!-- Main arrow -->
  <polygon id="arrow" points="-10,-5 10,0 -10,5" fill="red" />
</svg>


</template>

<style scoped>

</style>