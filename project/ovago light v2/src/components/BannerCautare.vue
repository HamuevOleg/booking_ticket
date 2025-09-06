<script setup>
  import BaraCautare from './BaraCautare.vue';

  import NavigareCautare from './NavigareCautare.vue';

  // ====== Importare biblioteca paralax ======

  import { gsap } from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  import { onMounted } from "vue"

  gsap.registerPlugin(ScrollTrigger)


  onMounted(() => {

    // function extragereString(className, addClass) {
    //   let targetElement = document.querySelector(className) // Cautam elementul pentru a extrage textul
    //   let letters = targetElement.textContent.split('') // Divizam textul in litere
    //   const newArr = letters.map(char => char === " " ? "&nbsp;" : char); // Inlocuim spatiul cu simbol
    //   targetElement.innerHTML = ``// Stergem continutul din containerul de referinta

    //   newArr.forEach(element => { // pentru fiecare simbol creem ..
    //     let newDiv = document.createElement("div") // Creem un container div
    //     newDiv.classList.add(addClass) // Adaugam in fiecare div clasa
    //     newDiv.innerHTML += `${element}` // Adaugam divul creat in containerul
    //     targetElement.appendChild(newDiv) // Publicam in html
    //   })
    // }

    // extragereString(".titlu_cautare", "class_parallax") // Pornirea funtii cu clasele indicate

    // gsap.from(".class_parallax", {
    //   opacity:0,
    //   y:32,
    //   stagger:0.1,
    //   duration:0.8,
    //   // delay:0.4,
    //   ease:"back.inOut(4)",
    // })

    gsap.from(".class_parallax", {
      opacity:0,
      y:32,
      stagger:0.1,
      duration:1,
      // delay:0.4,
      ease:"back.inOut(4)",
    })

    gsap.set(".banner_cautare_group", {
      zIndex: 30
    })

    gsap.to(".banner_cautare_group", {
      scrollTrigger:{
        trigger: ".banner_cautare_group",
        pin: true,
        start: "-204px top",
        end: "+=480",
        // markers: true,

        pinSpacing: false,
      },
      zIndex: 30


    })


    // ======= aici este animatia pentru titlu

    gsap.to(".titlu_cautare", {
      scrollTrigger:{
        trigger: ".hot_offer_component",
        start: "top 55%",
        end: "+=200",
        // markers: true,
        scrub: true,
      },
      opacity:0,
      y:32,
      fontWeight:200,
    })

  })



</script>

<template>
  

  <div class="banner_cautare_group">
    <div class="titlu_cautare">
      <div class="class_parallax">Book</div> &nbsp;
      <div class="class_parallax">your</div> &nbsp;
      <div class="class_parallax">Travel</div>
    </div>

    <div class="taburi_cautare_group">
      <NavigareCautare/>
      <BaraCautare/>      
    </div>

  </div>


</template>

<style scoped>

  .banner_cautare_group{
    display: flex;
    flex-direction: column;
    justify-content: center;

    gap: 48px;

    margin: 108px 0px;
  }

  .taburi_cautare_group{
    display: flex;
    flex-direction: column;
    justify-content: center;

    gap: 32px;
  }

  .titlu_cautare{

    display: flex;
    justify-content: center;

    color: #000;
    text-align: center;
    font-family: Jost;
    font-size: 48px;
    font-style: normal;
    font-weight: 500;
    line-height: 56px;

  }

</style>
