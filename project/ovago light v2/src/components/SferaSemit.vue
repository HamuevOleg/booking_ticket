<script setup>

  import ZborAvion_1 from './ZborAvion_1.vue';
  import ZborAvion_2 from './ZborAvion_2.vue';

  // ====== Importare biblioteca paralax ======

  import { gsap } from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  import { onMounted } from "vue"

  gsap.registerPlugin(ScrollTrigger)


  onMounted(() => {

    gsap.to(".sfera", {
      scrollTrigger:{
        trigger: ".antet_bloc_principal",
        start: "top top",
        end: "200% top",
        // markers: true,
        scrub: true,
      },
      opacity:0,
      y:240,
      ease:"none"
    })

  })


</script>

<template>
  <div class="sfera">
    <div class="sfera_umbra"></div>

    <div class="zborul_1_positionare">
      <ZborAvion_1/>      
    </div>

    <div class="zborul_1_positionare">
      <ZborAvion_2/>      
    </div>

  </div>
</template>

<style scoped>

  .sfera{
    width: 1552px;
    height: 1552px;
    position: absolute;
    top: 142%;
    left: 50%;
    transform: translate(-50%, -50%);

    flex-shrink: 0;

    border-radius: 1552px;
    box-shadow: 0px 16px 48px 0px #FFF inset;

    background: url(/src/components/media/planeta_intreaga.jpg) rgb(19, 19, 19) 50% -132px / 86% 63% no-repeat;
    /* background: radial-gradient(58.51% 58.51% at 37.79% 19.59%, rgba(255, 255, 255, 0.00) 0%, rgba(93, 80, 180, 0.08) 65.8%), rgba(129, 110, 252, 0.03); */
  }
  .sfera_umbra{
    box-shadow: 0px 4px 4px 0px #FFF inset;
  }

  .zborul_1_positionare{
    position: absolute;
    top: 17%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 2;
  }

</style>
