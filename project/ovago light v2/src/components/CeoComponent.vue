<script setup>

  // ====== Importare biblioteca paralax ======

  import { gsap } from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  import { onMounted } from "vue"

  gsap.registerPlugin(ScrollTrigger)


  onMounted(() => {

    gsap.from(".ceo_card_group", {
      scrollTrigger:{
        trigger: ".ceo_card_list",
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
  <div class="ceo_card_list">

    <div class="ceo_card_group">

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Dallas
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Phoenix
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Denver
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>
      
    </div>

    <div class="ceo_card_group">

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Indianapolis
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Miami
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Houston
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

    </div>

    <div class="ceo_card_group">

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Jacksonville
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Las Vegas
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Atlanta
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

    </div>

    <div class="ceo_card_group">

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Dallas
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Phoenix
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Denver
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

    </div>

    <div class="ceo_card_group">

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Dallas
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Phoenix
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

      <div class="ceo_card">
        <div class="ceo_card_group_link">

          <div class="ceo_card_title_link_group">
            Denver
          </div>

          <div class="ceo_card_group_link">

            <div class="ceo_card_link">
              Flights
            </div>

            <div class="ceo_card_link">
              Cars
            </div>

            <div class="ceo_card_link">
              Hotels
            </div>

          </div>
        </div>

        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="16" viewBox="0 0 17 16" fill="none">
          <path d="M2.66699 5L8.59628 10.9293C8.63533 10.9683 8.69865 10.9683 8.7377 10.9293L14.667 5" stroke="black" stroke-width="3" stroke-linecap="round"/>
        </svg>

      </div>

    </div>

  </div>

  
</template>

<style scoped>

  .ceo_card_list{
    margin-top: 240px;
    display: flex;
    padding: 0px 132px;
    flex-direction: column;
    align-items: flex-start;
    gap: 24px;
    align-self: stretch;
  }

  .ceo_card_group{
    display: flex;
    align-items: center;
    gap: 32px;
    align-self: stretch;
  }

  .ceo_card{
    display: flex;
    padding: 48px 64px;
    justify-content: space-between;
    align-items: center;
    flex: 1 0 0;

    border-radius: 40px;
    background: #FFF;
    box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.08);

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1) ;

  }

  .ceo_card:hover{
    box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.12);
    transform: translateY(-4px);
  }
  .ceo_card_title_link_group{
    display: flex;
    width: 118px;
    align-items: center;

    color: #000;
    text-align: center;
    font-family: Jost;
    font-size: 16px;
    font-style: normal;
    font-weight: 600;
    line-height: 24px; /* 150% */
  }

  .ceo_card_group_link{
    display: flex;
    align-items: center;
    gap: 24px;
  }

  .ceo_card_link{
    display: flex;
    justify-content: center;
    align-items: center;

    color: #816EFC;
    text-align: center;
    font-family: Jost;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 24px; /* 150% */

    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .ceo_card_link:hover{
    color: #C7BFFF;
  }



</style>
