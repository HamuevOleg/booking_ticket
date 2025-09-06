<script setup>


document.addEventListener("DOMContentLoaded", () => {
  const path = document.getElementById("motionPath") // incarcam calea 
  const pathLength = path.getTotalLength() // obține lungimea totală a căii, pe parta curbata
  

  const dot = document.getElementById("dot") // adaugam elementul pentru animatie


  let progress = 0 // adaugam variabila pentru a anima
  const speed = 0.001 // indicam valoarea de crestere

  function animate() {
    progress += speed;
    if (progress > 1) progress = 0 // pentru a reporni animatia efect de loop

    const point = path.getPointAtLength(progress * pathLength) // Oferă coordonatele de-a lungul traseului la o anumită lungime
    dot.setAttribute("cx", point.x)
    dot.setAttribute("cy", point.y)

    requestAnimationFrame(animate) // Actualizați poziția cercului la fiecare cadru de animație
  }

  animate()
})


</script>

<template>

<svg width="600" height="400" viewBox="0 0 600 400">
  <!-- The path (trajectory) -->
  <path id="motionPath" d="M50,300 C150,100 450,100 550,300" stroke="black" fill="none"/>

  <!-- The object to animate -->
  <circle id="dot" r="10" fill="red" />
</svg>


</template>

<style scoped>

</style>
