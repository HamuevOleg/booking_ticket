<script setup>
  // ====== Importare biblioteca paralax ======

  import { gsap } from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  import { onMounted, } from "vue"

  gsap.registerPlugin(ScrollTrigger)


  onMounted(() => {

    gsap.from(".antetul_banner", {
      scrollTrigger:{
        trigger: ".antetul_banner",
        start: "top bottom",
        end: "+=480",
        // markers: true,
        scrub: true,
      },
      opacity:0,
      ease:"none",
      scale:0.4,
    })

    gsap.from(".content_parallax", {
      scrollTrigger:{
        trigger: ".antetul_banner",
        start: "center 70%",
        end: "center 55%",
        // markers: true,
        scrub: true,
      },
      opacity:0,
      ease:"none",
      y:-120,
    })

  })
   
</script>

<template>

  <div class="antetul_banner">

    <div class="container_video_cautare">


      <div class="titlu_principal content_parallax">
        Exceptional <span class="customer">customer</span> <br>
        <span class="customer">support</span> 24/7
      </div> 

      <div class="support_group content_parallax">

        <div class="support_componet">

          <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 40 40" fill="none">
            <path d="M7.16667 14.6667L3 18.8333L17.1667 33L38 12.1667L33.8333 8L17.1667 24.6667L7.16667 14.6667Z" fill="white"/>
          </svg>

          <div class="support_info">
            <div class="support_info_title">
              Real travel experts
            </div>

            <div class="support_info_text">
              We've been there, done it, got the shirt.
            </div>

          </div>

        </div> 
        
        <div class="support_componet"> 

          <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 40 40" fill="none">
            <path d="M7.16667 14.6667L3 18.8333L17.1667 33L38 12.1667L33.8333 8L17.1667 24.6667L7.16667 14.6667Z" fill="white"/>
          </svg>

          <div class="support_info">
            <div class="support_info_title">
              Always there for you
            </div>

            <div class="support_info_text">
              Our response times are among the fastest in the industry.
            </div>

          </div>

        </div>   

        <div class="support_componet">

          <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 40 40" fill="none">
            <path d="M7.16667 14.6667L3 18.8333L17.1667 33L38 12.1667L33.8333 8L17.1667 24.6667L7.16667 14.6667Z" fill="white"/>
          </svg>

          <div class="support_info">
            <div class="support_info_title">
              Real travel experts
            </div>

            <div class="support_info_text">
              We do the hard work, so you don't have to.
            </div>

          </div>

        </div>   
      </div>



      <video autoplay loop muted class="video_fundal">
        <source src="/src/components/media/banner_support.mp4" type="video/mp4">
      </video>
    </div>
  </div>


  
</template>
  

<style scoped>

  .antetul_banner{
    margin-top: 200px;
    display: flex;
    flex-direction: column;
  }


  .container_video_cautare{
    display: flex;
    padding: 0px 132px;
    height: 780px;
    flex-direction: column;

    justify-content: flex-start;

    position: relative;
  }

  video {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 1656px;
    height: 78vh;
    object-fit: cover; 
    z-index: -3; 
    border-radius: 48px;
  }


  .titlu_principal{
    padding-top: 364px;
    color: #FFF;
    text-align: center;
    font-family: Jost;
    font-size: 88px;
    font-style: normal;
    font-weight: 700;
    line-height: 88px; /* 100% */
    letter-spacing: 2.64px;
  }

  .customer{
    color: #FFF;
    font-family: Jost;
    font-size: 88px;
    font-style: normal;
    font-weight: 300;
    line-height: 88px;
    letter-spacing: 2.64px;
  }

  .support_group{
    margin-top: 48px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 32px;
  }

  .support_componet{
    display: flex;
    padding: 24px 42px;
    justify-content: center;
    align-items: center;
    gap: 40px;

    border-radius: 40px;
    background: rgba(104, 97, 155, 0.08);
    backdrop-filter: blur(16px);
  }

  .support_info{
    display: flex;
    width: 312px;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 8px;
  }

  .support_info_title{
    color: #FFF;
    font-family: Jost;
    font-size: 24px;
    font-style: normal;
    font-weight: 500;
    line-height: 32px; /* 133.333% */

    align-self: stretch;
  }

  .support_info_text{
    color: #FFF;
    font-family: Jost;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 24px; /* 150% */

    height: 48px;
    align-self: stretch;
  }


</style>
