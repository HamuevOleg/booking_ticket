<script setup>

import ZborAvion_3 from './ZborAvion_3.vue';

// ====== Importare biblioteca paralax ======

import { gsap } from "gsap"
import { ScrollTrigger } from "gsap/ScrollTrigger"
import { onMounted } from "vue"

gsap.registerPlugin(ScrollTrigger)


onMounted(() => {

  gsap.from(".submit_title_parallax", {
    scrollTrigger: {
      trigger: ".submit_component",
      start: "top bottom",
      end: "center 60%",
      //  markers: true,
      scrub: true,
      // toggleActions: "restart pause reverse pause"
    },
    y: -240,
    opacity: 0,
    scale: 0.4,
    stagger: {
      each: 0.2,
      from: 'end',
    },
    fontWeight: 100,
    ease: 'power1.inOut'
  })

  // gsap.from(".avion_zbor", {
  //   scrollTrigger:{
  //     trigger: ".submit_component",
  //     start: "top bottom",
  //     end: "+=200",
  //      markers: true,
  //     // scrub: true,
  //     // toggleActions: "restart pause reverse pause"
  //   },

  //   opacity:0,
  // })


  gsap.from(".submit_search_parallax", {
    scrollTrigger: {
      trigger: ".submit_component",
      start: "20% bottom",
      end: "center 60%",
      // markers: true,
      scrub: true,
      // toggleActions: "restart pause reverse pause"
    },
    y: 132,
    opacity: 0,
    scale: 0.8,
    stagger: 0.2,
    ease: "back.inOut",
  })


})

</script>

<template>

  <div class="submit_component">
    <ZborAvion_3 class="avion_zbor" />
    <div class="submit_title_element">
      <div class="submit_title_main submit_title_parallax">
        Get deals you won’t see anywhere else!
      </div>
      <div class="submit_subtitle_main submit_title_parallax">
        By providing your email you consent to receive occasional promotional <br> Emails from us
      </div>
    </div>

    <div class="submit_group_down">

      <div class="submit_search_bar submit_search_parallax">
        <div class="submit_icon_place">
          <svg class="svg_mail" xmlns="http://www.w3.org/2000/svg" width="32" height="33" viewBox="0 0 32 33"
            fill="none">
            <path fill-rule="evenodd" clip-rule="evenodd"
              d="M2.93333 6.5C2.41787 6.5 2 6.91787 2 7.43333V25.5667C2 26.0821 2.41787 26.5 2.93333 26.5H29.0667C29.5821 26.5 30 26.0821 30 25.5667V7.43333C30 6.91786 29.5821 6.5 29.0667 6.5H2.93333ZM3.33333 8.71868V24.224L11.2848 16.2725L3.33333 8.71868ZM4.27624 25.1667H27.7239L19.7491 17.1919L16.5518 20.2294C16.2431 20.5227 15.7586 20.5227 15.4498 20.2294L12.2517 17.1912L4.27624 25.1667ZM28.6667 24.2239V8.72027L20.7161 16.2733L28.6667 24.2239ZM27.6644 7.83333H4.33726L16.0008 18.9137L27.6644 7.83333Z"
              fill="black" />
          </svg>
          Enter e-mail
        </div>
        <div class="submit_button">
          Submit
        </div>
      </div>

      <div class="submit_card_group submit_search_parallax">
        <div class="submit_card">

          <div class="icon_container">
            <svg class="icon_info" xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 48 48"
              fill="none">
              <path
                d="M35.9265 38.3104L33.8696 40.3673L26.2507 25.892L18.0183 32.7435L19.4184 39.6287L18.0471 41L13.8948 34.1052L7 29.9529L8.37127 28.5816L15.2565 29.9817L22.108 21.7493L7.63271 14.1304L9.68961 12.0735L27.5931 16.2643L31.7069 12.1505C32.845 11.0123 38.8221 5.55303 40.6345 7.36545C42.447 9.17787 36.9877 15.155 35.8495 16.2931L31.7357 20.4069L35.9265 38.3104Z"
                fill="white" />
            </svg>

            <svg class="icon_background" xmlns="http://www.w3.org/2000/svg" width="116" height="116"
              viewBox="0 0 116 116" fill="none">
              <path
                d="M62.5554 2.6365C60.4486 -0.881041 55.3512 -0.878293 53.2515 2.64151L34.9431 33.3318C34.4891 34.0928 33.8553 34.7308 33.0973 35.1898L2.61069 53.6523C-0.881548 55.7672 -0.867456 60.8391 2.63649 62.9378L33.0064 81.1276C33.7726 81.5864 34.4136 82.2274 34.8724 82.9936L53.0622 113.363C55.1609 116.867 60.2328 116.882 62.3477 113.389L80.8102 82.9027C81.2692 82.1447 81.9072 81.5109 82.6682 81.0569L113.358 62.7485C116.878 60.6488 116.881 55.5513 113.364 53.4445L82.7544 35.1115C81.9883 34.6527 81.3473 34.0117 80.8885 33.2455L62.5554 2.6365Z"
                fill="url(#paint0_linear_439_2875)" fill-opacity="0.7" />
              <defs>
                <linearGradient id="paint0_linear_439_2875" x1="26.2864" y1="26.4661" x2="89.5342" y2="89.714"
                  gradientUnits="userSpaceOnUse">
                  <stop stop-color="#AB9FFF" />
                  <stop offset="1" stop-color="#FFDEF3" />
                </linearGradient>
              </defs>
            </svg>

          </div>

          <div class="submit_info_card_element">
            <div class="submit_info_title">
              My Trips
            </div>
            <div class="submit_info_body">
              Quickly find your booking reservations and redeem flight credits
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="none">
            <path d="M11 6L20.8586 15.8586C20.9367 15.9367 20.9367 16.0633 20.8586 16.1414L11 26" stroke="#816EFC"
              stroke-width="3" stroke-linecap="round" />
          </svg>

        </div>

        <div class="submit_card">

          <div class="icon_container">

            <svg class="icon_info" xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 48 48"
              fill="none">
              <path d="M36 20H38.0559C40.7865 20 43 22.2135 43 24.9441V31.0559C43 33.7865 40.7865 36 38.0559 36H36V20Z"
                fill="white" />
              <path d="M12 20H9.94405C7.21353 20 5 22.2135 5 24.9441V31.0559C5 33.7865 7.21353 36 9.94405 36H12V20Z"
                fill="white" />
              <path
                d="M45 32.1791V23C45 11.402 35.598 2 24 2V2C12.402 2 3 11.402 3 23V30.1065C3 37.7797 9.22035 44 16.8935 44V44"
                stroke="white" stroke-width="2" stroke-linecap="round" />
              <circle cx="19" cy="44" r="3" fill="white" />
            </svg>

            <svg class="icon_background" xmlns="http://www.w3.org/2000/svg" width="116" height="116"
              viewBox="0 0 116 116" fill="none">
              <path
                d="M105.811 17.5877C106.933 13.1141 102.877 9.06183 98.4068 10.1913L59.4336 20.0398C58.4672 20.284 57.4556 20.2873 56.4876 20.0496L17.5539 10.4856C13.094 9.3901 9.07107 13.4355 10.1888 17.8917L19.8768 56.5158C20.1212 57.4902 20.1212 58.5098 19.8768 59.4842L10.1888 98.1083C9.07107 102.565 13.094 106.61 17.5539 105.514L56.4876 95.9504C57.4556 95.7126 58.4672 95.716 59.4336 95.9602L98.4068 105.809C102.877 106.938 106.933 102.886 105.811 98.4124L96.0468 59.4842C95.8024 58.5098 95.8024 57.4902 96.0468 56.5158L105.811 17.5877Z"
                fill="url(#paint0_linear_439_3128)" fill-opacity="0.7" />
              <defs>
                <linearGradient id="paint0_linear_439_3128" x1="58.0091" y1="7.69294" x2="58.0091" y2="108.307"
                  gradientUnits="userSpaceOnUse">
                  <stop stop-color="#AB9FFF" />
                  <stop offset="1" stop-color="#FFDEF3" />
                </linearGradient>
              </defs>
            </svg>

          </div>

          <div class="submit_info_card_element">
            <div class="submit_info_title">
              Help Center
            </div>
            <div class="submit_info_body">
              We are always Here for you - reach us 24hrs a day, 7 days a week
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="none">
            <path d="M11 6L20.8586 15.8586C20.9367 15.9367 20.9367 16.0633 20.8586 16.1414L11 26" stroke="#816EFC"
              stroke-width="3" stroke-linecap="round" />
          </svg>

        </div>

      </div>

    </div>

  </div>

</template>

<style scoped>
.submit_component {
  margin-top: 320px;
  display: flex;
  padding: 0px 396px;
  flex-direction: column;
  align-items: center;
  gap: 48px;
  align-self: stretch;
  position: relative;
}

.avion_zbor {
  position: absolute;
  width: 1048px;
  top: -20%;
  left: 50%;

  transform: translate(-50%, -50%);

}

.submit_title_element {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 16px;
}

.submit_title_main {
  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 32px;
  font-style: normal;
  font-weight: 500;
  line-height: 40px;
  /* 125% */
}

.submit_subtitle_main {
  align-self: stretch;

  color: rgba(0, 0, 0, 0.48);
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  /* 150% */
  letter-spacing: 0.64px;

}

.submit_group_down {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 88px;
  align-self: stretch;
}

.submit_search_bar {
  display: flex;
  padding: 8px 8px 8px 64px;
  justify-content: space-between;
  align-items: center;
  align-self: stretch;

  border-radius: 52px;
  border: 1px solid rgba(33, 0, 93, 0.08);
  background: #FFF;
  box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.08);

  cursor: pointer;
  transition: box-shadow 400ms cubic-bezier(0.3, 0, 0, 1);

}

.submit_search_bar:hover {
  box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.08);
}

.submit_icon_place {
  display: flex;
  align-items: center;
  gap: 16px;

  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

/* .svg_mail{
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .submit_search_bar:hover .svg_mail{
    transform: translateX(-8px);
  } */

.submit_search_bar:hover .submit_icon_place {
  transform: translateX(-8px);
}

.submit_button {
  display: flex;
  padding: 24px 32px;
  align-items: center;
  gap: 12px;

  border-radius: 42px;
  background: #816EFC;

  color: #FFF;
  text-align: center;
  font-family: Jost;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;

  cursor: pointer;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.submit_button:hover {
  background: rgba(129, 110, 252, 0.80);
  padding: 24px 40px;
}

.submit_card_group {
  display: flex;
  align-items: flex-start;
  gap: 48px;
  align-self: stretch;
}


.submit_card {
  display: flex;
  padding: 24px 32px 24px 24px;
  justify-content: space-between;
  align-items: center;
  flex: 1 0 0;

  border-radius: 40px;
  background: #FFF;
  box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.08);

  cursor: pointer;
  transition: box-shadow 400ms cubic-bezier(0.3, 0, 0, 1),
    transform 400ms cubic-bezier(0.3, 0, 0, 1);
}

.submit_card:hover {
  box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.08);
  transform: translateY(-8px);
}

.icon_container {
  display: flex;
  width: 116px;
  height: 116px;
  align-items: center;
  justify-content: center;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.submit_card:hover .icon_container {
  transform: scale(0.92);
}

.icon_info {
  z-index: 2;
}

.icon_background {
  width: 116px;
  height: 116px;
  aspect-ratio: 1/1;

  position: absolute;
  /* transition: all 400ms cubic-bezier(0.3, 0, 0, 1); */

}

/* .submit_card:hover .icon_background{
    transform: rotate(45deg);
  } */


.submit_info_card_element {
  display: flex;
  padding: 0px 32px;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  gap: 16px;
  flex: 1 0 0;
}

.submit_info_title {
  color: #000;
  font-family: Jost;
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 32px;
  /* 160% */
}

.submit_info_body {
  align-self: stretch;

  color: rgba(0, 0, 0, 0.48);
  font-family: Jost;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 20px;
  /* 142.857% */
}
</style>
