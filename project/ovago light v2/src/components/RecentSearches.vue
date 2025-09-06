<script setup>


  // ====== Importare biblioteca paralax ======

  import { gsap } from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  import { onMounted, } from "vue"

  gsap.registerPlugin(ScrollTrigger)


  onMounted(() => {


    gsap.from(".card_recent_parallax", {
      opacity:0,
      y:80,
      duration:1.6,
      delay:0.6,
      ease:"back.inOut(4)",
      stagger:0.2,
    })

    gsap.from(".titlu_recent_parallax", {
      opacity:0,
      y:-32,
      duration:1.2,
      delay:0.6,
      ease:"back.inOut(4)",
      stagger:0.2,
    })

    gsap.to(".card_group", {
      scrollTrigger:{
        trigger: ".recent_search_component",
        start: "top 60%",
        end: "+=100",
        // markers: true,
        scrub: true,
      },
      opacity:0,
      ease:"none"
    })

    gsap.to(".titlu_recent", {
      scrollTrigger:{
        trigger: ".recent_search_component",
        start: "top 70%",
        end: "+=200",
        // markers: true,
        scrub: true,
      },
      opacity:0,
      ease:"none"
    })

  })

</script>

<template>

  <div class="recent_search_component">
    <div class="titlu_recent_parallax">
      <div class="titlu_recent">
        Your recent searches
      </div>
    </div>



    <div class="card_group">

      <div class="card_recent_parallax">

        <div class="card_component">

          <svg xmlns="http://www.w3.org/2000/svg" width="51" height="51" viewBox="0 0 51 51" fill="none">
            <path d="M42.9216 45.2538L40.0201 48.1553L29.2031 27.6667L17.586 37.3272L19.5872 47.0657L17.6528 49L11.7607 39.2393L2 33.3472L3.93433 31.4128L13.6728 33.414L23.3333 21.7969L2.84468 10.9799L5.74618 8.07837L31.0707 14.0595L36.8737 8.25653C38.4792 6.65104 46.9122 -1.04827 49.4802 1.51977C52.0483 4.08781 44.349 12.5208 42.7435 14.1263L36.9405 19.9293L42.9216 45.2538Z" stroke="#AB9FFF" stroke-width="1.5"/>
          </svg>

          <div class="info_card">
            <div class="info_card_title">
              Flights from to Paris
            </div>
            <div class="info_card_body">
              Thu, Apr 17 - Thu, Apr 24
            </div>
            <div class="info_card_body">
              Roundtrip • 1 traveler
            </div>
          </div>
        </div> 

      </div>

      <div class="card_recent_parallax">
        <div class="card_component">

          <svg xmlns="http://www.w3.org/2000/svg" width="51" height="51" viewBox="0 0 51 51" fill="none">
            <path d="M42.9216 45.2538L40.0201 48.1553L29.2031 27.6667L17.586 37.3272L19.5872 47.0657L17.6528 49L11.7607 39.2393L2 33.3472L3.93433 31.4128L13.6728 33.414L23.3333 21.7969L2.84468 10.9799L5.74618 8.07837L31.0707 14.0595L36.8737 8.25653C38.4792 6.65104 46.9122 -1.04827 49.4802 1.51977C52.0483 4.08781 44.349 12.5208 42.7435 14.1263L36.9405 19.9293L42.9216 45.2538Z" stroke="#AB9FFF" stroke-width="1.5"/>
          </svg>

          <div class="info_card">
            <div class="info_card_title">
              Flights from to Paris
            </div>
            <div class="info_card_body">
              Thu, Apr 17 - Thu, Apr 24
            </div>
            <div class="info_card_body">
              Roundtrip • 1 traveler
            </div>

          </div>
        </div>   
      </div>

      <div class="card_recent_parallax">
        <div class="card_component">

          <svg xmlns="http://www.w3.org/2000/svg" width="51" height="51" viewBox="0 0 51 51" fill="none">
            <path d="M42.9216 45.2538L40.0201 48.1553L29.2031 27.6667L17.586 37.3272L19.5872 47.0657L17.6528 49L11.7607 39.2393L2 33.3472L3.93433 31.4128L13.6728 33.414L23.3333 21.7969L2.84468 10.9799L5.74618 8.07837L31.0707 14.0595L36.8737 8.25653C38.4792 6.65104 46.9122 -1.04827 49.4802 1.51977C52.0483 4.08781 44.349 12.5208 42.7435 14.1263L36.9405 19.9293L42.9216 45.2538Z" stroke="#AB9FFF" stroke-width="1.5"/>
          </svg>

          <div class="info_card">
            <div class="info_card_title">
              Flights from to Paris
            </div>
            <div class="info_card_body">
              Thu, Apr 17 - Thu, Apr 24
            </div>
            <div class="info_card_body">
              Roundtrip • 1 traveler
            </div>

          </div>

        </div>  
      </div>

  



  

    </div>
  </div>

  
</template>

<style scoped>

  .recent_search_component{
    margin-top: 224px;
    display: flex;
    position: relative;
    flex-direction: column;
    gap: 56px;
    z-index: 2;
  }

  .card_group{
    display: flex;
    padding: 0px 332px 0px 332px;
    align-items: center;
    gap: 32px;
  }

  .titlu_recent{
    color: #FFF;
    text-align: center;
    font-family: Jost;
    font-size: 32px;
    font-style: normal;
    font-weight: 400;
    line-height: 32px; /* 100% */
  }

  .card_component{
    display: flex;
    padding: 24px 40px;
    justify-content: center;
    align-items: center;
    gap: 40px;

    border-radius: 40px;
    /* border: 1px solid rgba(255, 255, 255, 0.24); */
    background: rgba(104, 97, 155, 0.08);
    backdrop-filter: blur(16px);

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .card_component:hover{
    background: rgba(199, 191, 255, 0.16);
    transform: translateY(-12px);
  }

  .info_card{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 8px;
  }

  .info_card_title{
    color: #FFF;
    font-family: Jost;
    font-size: 24px;
    font-style: normal;
    font-weight: 500;
    line-height: 32px; /* 133.333% */

    align-self: stretch;
    white-space: none;

  }

  .info_card_body{
    color: rgba(255, 255, 255, 0.64);
    font-family: Jost;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 24px; /* 150% */

    align-self: stretch;
  }

</style>