<script setup>

  // ====== Importare biblioteca paralax ======

  import { gsap } from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  import { onMounted } from "vue"

  gsap.registerPlugin(ScrollTrigger)


  onMounted(() => {

    gsap.from(".may_main_title", {
      scrollTrigger:{
        trigger: ".may_component",
        start: "top bottom",
        end: "center 60%",
        //  markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
      },
      y:-240,
      opacity:0,
      scale:0.4,
      stagger: 0.1,
      fontWeight:100,
      ease: 'power1.inOut'
    })

    gsap.from(".may_parallax_dreapta", {
      scrollTrigger:{
        trigger: ".may_component",
        start: "20% bottom",
        end: "110% bottom",
        // markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
      },
      y:32,
      x:132,
      opacity:0,
      scale:0.8,
      stagger:0.2,
      // ease:"back.inOut",
    })

    gsap.from(".may_parallax_stinga", {
      scrollTrigger:{
        trigger: ".may_component",
        start: "20% bottom",
        end: "110% bottom",
        // markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
      },
      y:32,
      x:-132,
      opacity:0,
      scale:0.8,
      stagger:0.2,
      // ease:"back.inOut",
    })

    gsap.from(".may_parallax_centru", {
      scrollTrigger:{
        trigger: ".may_component",
        start: "20% bottom",
        end: "110% bottom",
        // markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
      },
      y:32,
      opacity:0,
      scale:0.8,
      stagger:0.2,
      ease:"back.inOut",
    })


  })
  
</script>

<template>
  <div class="may_component">
    <div class="may_main_title">
      You may be interested in
    </div>
      <div class="may_deals_group">

        <div class="may_card may_parallax_stinga">
          <div class="may_imag_card">
            <div class="may_mag">

            </div>

          </div>

          <div class="may_info_elem">
            <div class="may_info_title">
              Top Airline Deals
            </div>
            <div class="may_link">
              View More
              <svg class="may_icon_link" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M5 2L10.9293 7.92929C10.9683 7.96834 10.9683 8.03166 10.9293 8.07071L5 14" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>

          </div>

        </div>

        <div class="may_card may_parallax_centru">
          <div class="may_imag_card">
            <div class="may_mag_2">

            </div>

          </div>

          <div class="may_info_elem">
            <div class="may_info_title">
              Student Travel Deals
            </div>
            <div class="may_link">
              View More
              <svg class="may_icon_link" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M5 2L10.9293 7.92929C10.9683 7.96834 10.9683 8.03166 10.9293 8.07071L5 14" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>

          </div>

        </div>

        <div class="may_card may_parallax_dreapta">
          <div class="may_imag_card">
            <div class="may_mag_3">

            </div>

          </div>

          <div class="may_info_elem">
            <div class="may_info_title">
              Business Class Deals
            </div>
            <div class="may_link">
              View More
              <svg class="may_icon_link" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M5 2L10.9293 7.92929C10.9683 7.96834 10.9683 8.03166 10.9293 8.07071L5 14" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>

          </div>

        </div>

      </div>

      <div class="may_deals_group">
        
        <div class="may_card may_parallax_stinga">
          <div class="may_imag_card">
            <div class="may_mag_4">

            </div>

          </div>

          <div class="may_info_elem">
            <div class="may_info_title">
              First Class Deals
            </div>
            <div class="may_link">
              View More
              <svg class="may_icon_link" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M5 2L10.9293 7.92929C10.9683 7.96834 10.9683 8.03166 10.9293 8.07071L5 14" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>

          </div>

        </div>

        <div class="may_card may_parallax_centru">
          <div class="may_imag_card">
            <div class="may_mag_5">

            </div>

          </div>

          <div class="may_info_elem">
            <div class="may_info_title">
              Last Minute Flight 
            </div>
            <div class="may_link">
              View More
              <svg class="may_icon_link" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M5 2L10.9293 7.92929C10.9683 7.96834 10.9683 8.03166 10.9293 8.07071L5 14" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>

          </div>

        </div>

        <div class="may_card may_parallax_dreapta">
          <div class="may_imag_card">
            <div class="may_mag_6">

            </div>

          </div>

          <div class="may_info_elem">
            <div class="may_info_title">
              Round-the-World 
            </div>
            <div class="may_link">
              View More
              <svg class="may_icon_link" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M5 2L10.9293 7.92929C10.9683 7.96834 10.9683 8.03166 10.9293 8.07071L5 14" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>

          </div>

        </div>

      </div>
      <div class="may_deals_group">
        
        <div class="may_card may_parallax_stinga">
          <div class="may_imag_card">
            <div class="may_mag_7">

            </div>

          </div>

          <div class="may_info_elem">
            <div class="may_info_title">
              Group Travel Deals
            </div>
            <div class="may_link">
              View More
              <svg class="may_icon_link" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M5 2L10.9293 7.92929C10.9683 7.96834 10.9683 8.03166 10.9293 8.07071L5 14" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>

          </div>

        </div>

        <div class="may_card may_parallax_centru">
          <div class="may_imag_card">
            <div class="may_mag_8">

            </div>

          </div>

          <div class="may_info_elem">
            <div class="may_info_title">
              Senior Travel Deals
            </div>
            <div class="may_link">
              View More
              <svg class="may_icon_link" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M5 2L10.9293 7.92929C10.9683 7.96834 10.9683 8.03166 10.9293 8.07071L5 14" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>

          </div>

        </div>

        <div class="may_card may_parallax_dreapta">
          <div class="may_imag_card">
            <div class="may_mag_9">

            </div>

          </div>

          <div class="may_info_elem">
            <div class="may_info_title">
              Veteran Flight 
            </div>
            <div class="may_link">
              View More
              <svg class="may_icon_link" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                <path d="M5 2L10.9293 7.92929C10.9683 7.96834 10.9683 8.03166 10.9293 8.07071L5 14" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>

          </div>

        </div>

      </div>


  </div>


</template>

<style scoped>

  .may_component{
    margin-top: 240px;
    display: flex;
    padding: 0px 132px;
    flex-direction: column;
    align-items: center;
    gap: 48px;
    align-self: stretch;
  }

  .may_main_title{
    color: #000;
    text-align: center;
    font-family: Jost;
    font-size: 32px;
    font-style: normal;
    font-weight: 500;
    line-height: 40px; /* 125% */
  }


  .may_deals_group{
    display: flex;
    align-items: flex-start;
    gap: 48px;
    align-self: stretch;
  }

  .may_card{
    display: flex;
    padding-right: 40px;
    align-items: center;
    gap: 40px;
    flex: 1 0 0;

    border-radius: 40px;
    background: #FFF;
    box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.12);
    overflow: hidden;

    cursor: pointer;
    transition: box-shadow 600ms cubic-bezier(0.3, 0, 0, 1); 
    /* transform 600ms cubic-bezier(0.3, 0, 0, 1); */

  }

  .may_card:hover{
    box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.12);
    /* transform: translateY(-4px) */
  }

  .may_imag_card{
    display: flex;
    width: 200px;
    height: 200px;
    justify-content: center;
    align-items: center;
    
  }

  /* Prima imagine */

  .may_mag{
    width: 200px;
    height: 200px;
    flex-shrink: 0;

    overflow: hidden; 
    position: relative;
  }

  .may_mag::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/may_1.jpg) lightgray center / 100% 100% no-repeat;

    background-size: 108%; 
    transition: all 600ms cubic-bezier(0.3, 0, 0, 1); 
  }

  .may_card:hover .may_mag::before {
    background-size: 100%; 
  } 

  /* Imaginea doi */

  .may_mag_2{
    width: 200px;
    height: 200px;
    flex-shrink: 0;

    overflow: hidden; 
    position: relative;
  }

  .may_mag_2::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/may_2.jpg) lightgray center / 100% 100% no-repeat;

    background-size: 108%; 
    transition: all 600ms cubic-bezier(0.3, 0, 0, 1); 
  }

  .may_card:hover .may_mag_2::before {
    background-size: 100%; 
  } 

  /* Imaginea trei */

  .may_mag_3{
    width: 200px;
    height: 200px;
    flex-shrink: 0;

    overflow: hidden; 
    position: relative;
  }

  .may_mag_3::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/may_3.jpg) lightgray center / 100% 100% no-repeat;

    background-size: 108%; 
    transition: all 600ms cubic-bezier(0.3, 0, 0, 1); 
  }

  .may_card:hover .may_mag_3::before {
    background-size: 100%; 
  } 

  /* Imaginea patru */

  .may_mag_4{
    width: 200px;
    height: 200px;
    flex-shrink: 0;

    overflow: hidden; 
    position: relative;
  }

  .may_mag_4::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/may_4.jpg) lightgray center / 100% 100% no-repeat;

    background-size: 108%; 
    transition: all 600ms cubic-bezier(0.3, 0, 0, 1); 
  }

  .may_card:hover .may_mag_4::before {
    background-size: 100%; 
  } 

  /* Imaginea cinci */

  .may_mag_5{
    width: 200px;
    height: 200px;
    flex-shrink: 0;

    overflow: hidden; 
    position: relative;
  }

  .may_mag_5::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/may_5.jpg) lightgray center / 100% 100% no-repeat;

    background-size: 108%; 
    transition: all 600ms cubic-bezier(0.3, 0, 0, 1); 
  }

  .may_card:hover .may_mag_5::before {
    background-size: 100%; 
  } 

  /* Imaginea sase */

  .may_mag_6{
    width: 200px;
    height: 200px;
    flex-shrink: 0;

    overflow: hidden; 
    position: relative;
  }

  .may_mag_6::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/may_6.jpg) lightgray center / 100% 100% no-repeat;

    background-size: 108%; 
    transition: all 600ms cubic-bezier(0.3, 0, 0, 1); 
  }

  .may_card:hover .may_mag_6::before {
    background-size: 100%; 
  } 

  /* Imaginea sapte */

  .may_mag_7{
    width: 200px;
    height: 200px;
    flex-shrink: 0;

    overflow: hidden; 
    position: relative;
  }

  .may_mag_7::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/may_7.jpg) lightgray center / 100% 100% no-repeat;

    background-size: 108%; 
    transition: all 600ms cubic-bezier(0.3, 0, 0, 1); 
  }

  .may_card:hover .may_mag_7::before {
    background-size: 100%; 
  } 

  /* Imaginea opt */

  .may_mag_8{
    width: 200px;
    height: 200px;
    flex-shrink: 0;

    overflow: hidden; 
    position: relative;
  }

  .may_mag_8::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/may_8.jpg) lightgray center / 100% 100% no-repeat;

    background-size: 108%; 
    transition: all 600ms cubic-bezier(0.3, 0, 0, 1); 
  }

  .may_card:hover .may_mag_8::before {
    background-size: 100%; 
  } 

  /* Imaginea noua */

  .may_mag_9{
    width: 200px;
    height: 200px;
    flex-shrink: 0;

    overflow: hidden; 
    position: relative;
  }

  .may_mag_9::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/may_9.jpg) lightgray center / 100% 100% no-repeat;

    background-size: 108%; 
    transition: all 600ms cubic-bezier(0.3, 0, 0, 1); 
  }

  .may_card:hover .may_mag_9::before {
    background-size: 100%; 
  } 

  /* info_element */

  .may_info_elem{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 16px;
  }

  .may_info_title{
    color: #000;
    font-family: Jost;
    font-size: 24px;
    font-style: normal;
    font-weight: 500;
    line-height: 32px; /* 133.333% */
  }
  
  .may_link{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 4px;

    color: #816EFC;
    text-align: center;
    font-family: Jost;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 24px; /* 133.333% */
  }
  .may_icon_link{
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .may_link:hover .may_icon_link{
    transform: translateX(8px);
  }



</style>
