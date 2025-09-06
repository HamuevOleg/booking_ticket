<script setup>

  // ====== Importare biblioteca paralax ======

  import { gsap } from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  import { onMounted } from "vue"

  gsap.registerPlugin(ScrollTrigger)


  onMounted(() => {

    gsap.to(".card_hot_group_sec", {
      scrollTrigger:{
        trigger: ".hot_offer_component_sec",
        start: "top bottom",
        end: "+=100",
        // markers: true,
        scrub: true,
      },
      y:-72,
      // opacity:0,
      ease:"none"
    })

  })

</script>

<template>

  <div class="hot_offer_component_sec">

    <div class="card_hot_group_sec">

      <div class="card_hot_sec">

        <div class="card_hot_imag_sec"></div>

        <div class="card_hot_info_sec">
          <div class="card_hot_info_body_sec">
            You can Bundle & Save up to $974 with package
          </div>

          <div class="action_hot_element_sec">
            Book now
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="17" viewBox="0 0 16 17" fill="none">
              <path d="M5 2.5L10.9293 8.42929C10.9683 8.46834 10.9683 8.53166 10.9293 8.57071L5 14.5" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
            </svg>

          </div>

        </div>

      </div> 

      <div class="card_hot_sec">

        <div class="card_hot_imag_2_sec"></div>

        <div class="card_hot_info_sec">
          <div class="card_hot_info_body_sec">
            Cleared for takeoff: Southwest Airlines now on Expedia
          </div>

          <div class="action_hot_element_sec">
            Book now
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="17" viewBox="0 0 16 17" fill="none">
              <path d="M5 2.5L10.9293 8.42929C10.9683 8.46834 10.9683 8.53166 10.9293 8.57071L5 14.5" stroke="#816EFC" stroke-width="2" stroke-linecap="round"/>
            </svg>

          </div>

        </div>

      </div> 

      
    </div>
   
  </div>



  
</template>

<style scoped>

  .hot_offer_component_sec{
    margin-top: 120px;
    display: flex;
    position: relative;
    flex-direction: column;
    gap: 56px;
    z-index: 2;
  }


  .card_hot_group_sec{
    display: flex;
    align-items: center;
    gap: 48px;
    padding: 0px 312px 0px 312px;
    justify-content: center;
  }

  .card_hot_sec{
    display: flex;
    width: 624px;
    padding-right: 40px;
    align-items: center;
    gap: 40px;

    border-radius: 40px;
    background: #FFF;
    box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.12);

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .card_hot_sec:hover{
    box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.08);
    transform: translateY(-8px);
  }

  .card_hot_info_sec{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 16px;
  }

  .card_hot_imag_sec{
    width: 312px;
    height: 200px;
    flex-shrink: 0;
    border-radius: 40px 0px 0px 40px;
    background: url(/src/components/media/hot_3.jpg) lightgray 0px 0px / 100% 100% no-repeat;
  }

  .card_hot_imag_2_sec{
    width: 312px;
    height: 200px;
    flex-shrink: 0;
    border-radius: 40px 0px 0px 40px;
    background: url(/src/components/media/hot_4.jpg) lightgray 0px 0px / 100% 100% no-repeat;
  }

  .card_hot_info_body_sec{

    width: 216px;

    color: #000;
    font-family: Jost;
    font-size: 20px;
    font-style: normal;
    font-weight: 500;
    line-height: 32px; /* 160% */
  }

  .action_hot_element_sec{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 8px;

    color: #816EFC;
    text-align: center;
    font-family: Jost;
    font-size: 18px;
    font-style: normal;
    font-weight: 500;
    line-height: 24px; /* 133.333% */

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .action_hot_element_sec:hover{
    gap: 16px;
  }
  

</style>
