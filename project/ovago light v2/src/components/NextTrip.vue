<script setup>
// ====== Importare biblioteca paralax ======

import { gsap, } from "gsap"
import { ScrollTrigger } from "gsap/ScrollTrigger"
import { onMounted } from "vue"

gsap.registerPlugin(ScrollTrigger)


onMounted(() => {

  gsap.set(".card_next", {
    y: 240,
    // x:240,
    scale: 0.6,
    opacity: -1
  })

  gsap.to(".card_next", {
    scrollTrigger: {
      trigger: ".next_component",
      start: "top bottom",
      end: "center center",
      // markers: true,
      scrub: true,
      // toggleActions: "restart pause reverse pause"

    },
    y: 0,
    x: 0,
    ease: 'none',
    stagger: 0.1,
    scale: 1,
    opacity: 1,
    // ease:"back.inOut(1)",
  })


  gsap.from(".next_parallax", {
    scrollTrigger: {
      trigger: ".next_component",
      start: "top 80%",
      end: "top center",
      // markers: true,
      scrub: true
    },
    y: -180,
    ease: "power2inOut",
    opacity: 0,
    scale: 0.6,
    stagger: {
      each: 0.2,
      from: 'end',
    },
    fontWeight: 200,
    // rotation:30,
  })


})

</script>

<template>
  <div class="next_component">
    <div class="titlu_taburi">
      <div class="titlu_inspiration next_parallax">
        Discover travel deals to top vacation spots.
      </div>

      <div class="containerul_taburi next_parallax">

        <div class="tab_elemet">
          <div class="tab_label">
            Paris
          </div>
          <div class="linie_tab_default"></div>
        </div>

        <div class="tab_elemet">
          <div class="tab_label">
            Singapore
          </div>
          <div class="linie_tab_default"></div>
        </div>

        <div class="tab_elemet">
          <div class="tab_label label_default ">
            Antalya
          </div>
          <div class="linie_tab"></div>
        </div>

        <div class="tab_elemet">
          <div class="tab_label ">
            Santorini
          </div>
          <div class="linie_tab_default"></div>
        </div>

        <div class="tab_elemet ">
          <div class="tab_label ">
            Amsterdam
          </div>
          <div class="linie_tab_default"></div>
        </div>

      </div>

    </div>

    <div class="next_group">
      <div class="card_next imagine_hotel_1">
        <div class="card_next_price">
          <div class="card_next_city_title">
            Concorde De Luxe Resort
          </div>
          <div class="card_next_city_title_2">
            All Inclusive + Flight
          </div>


          <div class="rating_star_group">

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

          </div>

          <div class="avion_container_0">

            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M12 2.5L14.1329 9.06434H21.035L15.4511 13.1213L17.584 19.6857L12 15.6287L6.41604 19.6857L8.54892 13.1213L2.96496 9.06434H9.86712L12 2.5Z"
                stroke="white" />
            </svg>

            8.8/10 Excellent (1,317)

          </div>

          <div class="avion_container">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                stroke="white" />
            </svg>

            Chisinau (RMO) - Antalya (AYT)

          </div>

          <div class="avion_container_2">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M12 2.5C9.23858 2.5 7 4.73858 7 7.5C7 10.2614 9.23858 12.5 12 12.5C14.7614 12.5 17 10.2614 17 7.5C17 4.73858 14.7614 2.5 12 2.5ZM8 7.5C8 5.29086 9.79086 3.5 12 3.5C14.2091 3.5 16 5.29086 16 7.5C16 9.70914 14.2091 11.5 12 11.5C9.79086 11.5 8 9.70914 8 7.5Z"
                fill="white" />
              <path
                d="M4.5 21C4.5 19.2657 5.56191 18.1567 7.08453 17.454C8.62004 16.7453 10.5405 16.5 12 16.5C13.4595 16.5 15.38 16.7453 16.9155 17.454C18.4381 18.1567 19.5 19.2657 19.5 21C19.5 21.2761 19.7239 21.5 20 21.5C20.2761 21.5 20.5 21.2761 20.5 21C20.5 18.7343 19.0619 17.3433 17.3345 16.546C15.62 15.7547 13.5405 15.5 12 15.5C10.4595 15.5 8.37996 15.7547 6.66547 16.546C4.93809 17.3433 3.5 18.7343 3.5 21C3.5 21.2761 3.72386 21.5 4 21.5C4.27614 21.5 4.5 21.2761 4.5 21Z"
                fill="white" />
            </svg>

            per traveler

          </div>

          <div class="avion_container_3">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M8 14C8.55229 14 9 13.5523 9 13C9 12.4477 8.55229 12 8 12C7.44772 12 7 12.4477 7 13C7 13.5523 7.44772 14 8 14Z"
                fill="white" />
              <path
                d="M9 17C9 17.5523 8.55229 18 8 18C7.44772 18 7 17.5523 7 17C7 16.4477 7.44772 16 8 16C8.55229 16 9 16.4477 9 17Z"
                fill="white" />
              <path
                d="M12 18C12.5523 18 13 17.5523 13 17C13 16.4477 12.5523 16 12 16C11.4477 16 11 16.4477 11 17C11 17.5523 11.4477 18 12 18Z"
                fill="white" />
              <path
                d="M13 13C13 13.5523 12.5523 14 12 14C11.4477 14 11 13.5523 11 13C11 12.4477 11.4477 12 12 12C12.5523 12 13 12.4477 13 13Z"
                fill="white" />
              <path
                d="M16 14C16.5523 14 17 13.5523 17 13C17 12.4477 16.5523 12 16 12C15.4477 12 15 12.4477 15 13C15 13.5523 15.4477 14 16 14Z"
                fill="white" />
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M6 0.5C6.27614 0.5 6.5 0.723858 6.5 1V2.72637C6.66345 2.69868 6.83201 2.67452 7.00593 2.65339C8.2688 2.49999 9.87976 2.5 11.965 2.5H12.035C14.1202 2.5 15.7312 2.49999 16.9941 2.65339C17.168 2.67452 17.3365 2.69868 17.5 2.72637V1C17.5 0.723858 17.7239 0.5 18 0.5C18.2761 0.5 18.5 0.723858 18.5 1V2.96349C19.0965 3.15423 19.6138 3.42649 20.072 3.81777C20.2911 4.00489 20.4951 4.20894 20.6822 4.42804C21.3709 5.2344 21.6909 6.22436 21.8466 7.50593C22 8.7688 22 10.3798 22 12.4651V12.5349C22 14.6202 22 16.2312 21.8466 17.4941C21.6909 18.7756 21.3709 19.7656 20.6822 20.572C20.4951 20.7911 20.2911 20.9951 20.072 21.1822C19.2656 21.8709 18.2756 22.1909 16.9941 22.3466C15.7312 22.5 14.1202 22.5 12.0349 22.5H11.9651C9.87978 22.5 8.2688 22.5 7.00593 22.3466C5.72436 22.1909 4.7344 21.8709 3.92804 21.1822C3.70894 20.9951 3.50489 20.7911 3.31777 20.572C2.62907 19.7656 2.30907 18.7756 2.15339 17.4941C1.99999 16.2312 2 14.6202 2 12.535V12.465C2 10.3798 1.99999 8.7688 2.15339 7.50593C2.30907 6.22436 2.62907 5.2344 3.31777 4.42804C3.50489 4.20894 3.70894 4.00489 3.92804 3.81777C4.38616 3.42649 4.90355 3.15423 5.5 2.96349V1C5.5 0.723858 5.72386 0.5 6 0.5ZM17.5 3.7424V5C17.5 5.27614 17.7239 5.5 18 5.5C18.2761 5.5 18.5 5.27614 18.5 5V4.02566C18.8562 4.16964 19.1565 4.35099 19.4225 4.57817C19.6018 4.73127 19.7687 4.89823 19.9218 5.07748C20.4127 5.65225 20.6897 6.38731 20.8378 7.5H3.16219C3.31034 6.38731 3.58727 5.65225 4.07817 5.07748C4.23127 4.89823 4.39823 4.73127 4.57748 4.57817C4.84348 4.35099 5.1438 4.16964 5.5 4.02566V5C5.5 5.27614 5.72386 5.5 6 5.5C6.27614 5.5 6.5 5.27614 6.5 5V3.7424C6.69519 3.70508 6.90348 3.67319 7.12651 3.6461C8.32212 3.50086 9.87251 3.5 12 3.5C14.1275 3.5 15.6779 3.50086 16.8735 3.6461C17.0965 3.67319 17.3048 3.70508 17.5 3.7424ZM3 12.5C3 10.8564 3.00052 9.55724 3.06772 8.5H20.9323C20.9995 9.55724 21 10.8564 21 12.5C21 14.6275 20.9991 16.1779 20.8539 17.3735C20.7101 18.5574 20.4311 19.3262 19.9218 19.9225C19.7687 20.1018 19.6018 20.2687 19.4225 20.4218C18.8262 20.9311 18.0574 21.2101 16.8735 21.3539C15.6779 21.4991 14.1275 21.5 12 21.5C9.87251 21.5 8.32212 21.4991 7.12651 21.3539C5.94255 21.2101 5.17376 20.9311 4.57748 20.4218C4.39823 20.2687 4.23127 20.1018 4.07817 19.9225C3.5689 19.3262 3.28992 18.5574 3.1461 17.3735C3.00086 16.1779 3 14.6275 3 12.5Z"
                fill="white" />
            </svg>

            Fri, Jun 27 - Fri, Jul 4 (7 nights)

          </div>

          <div class="card_next_info">
            <div class="card_next_from">
              $850
            </div>

            <div class="card_next_price_star">
              $450
            </div>

          </div>


        </div>

      </div>

      <div class="card_next imagine_hotel_2">
        <div class="card_next_price">
          <div class="card_next_city_title">
            Concorde De Luxe Resort
          </div>
          <div class="card_next_city_title_2">
            All Inclusive + Flight
          </div>


          <div class="rating_star_group">

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

          </div>

          <div class="avion_container_0">

            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M12 2.5L14.1329 9.06434H21.035L15.4511 13.1213L17.584 19.6857L12 15.6287L6.41604 19.6857L8.54892 13.1213L2.96496 9.06434H9.86712L12 2.5Z"
                stroke="white" />
            </svg>

            8.8/10 Excellent (1,317)

          </div>

          <div class="avion_container">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                stroke="white" />
            </svg>

            Chisinau (RMO) - Antalya (AYT)

          </div>

          <div class="avion_container_2">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M12 2.5C9.23858 2.5 7 4.73858 7 7.5C7 10.2614 9.23858 12.5 12 12.5C14.7614 12.5 17 10.2614 17 7.5C17 4.73858 14.7614 2.5 12 2.5ZM8 7.5C8 5.29086 9.79086 3.5 12 3.5C14.2091 3.5 16 5.29086 16 7.5C16 9.70914 14.2091 11.5 12 11.5C9.79086 11.5 8 9.70914 8 7.5Z"
                fill="white" />
              <path
                d="M4.5 21C4.5 19.2657 5.56191 18.1567 7.08453 17.454C8.62004 16.7453 10.5405 16.5 12 16.5C13.4595 16.5 15.38 16.7453 16.9155 17.454C18.4381 18.1567 19.5 19.2657 19.5 21C19.5 21.2761 19.7239 21.5 20 21.5C20.2761 21.5 20.5 21.2761 20.5 21C20.5 18.7343 19.0619 17.3433 17.3345 16.546C15.62 15.7547 13.5405 15.5 12 15.5C10.4595 15.5 8.37996 15.7547 6.66547 16.546C4.93809 17.3433 3.5 18.7343 3.5 21C3.5 21.2761 3.72386 21.5 4 21.5C4.27614 21.5 4.5 21.2761 4.5 21Z"
                fill="white" />
            </svg>

            per traveler

          </div>

          <div class="avion_container_3">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M8 14C8.55229 14 9 13.5523 9 13C9 12.4477 8.55229 12 8 12C7.44772 12 7 12.4477 7 13C7 13.5523 7.44772 14 8 14Z"
                fill="white" />
              <path
                d="M9 17C9 17.5523 8.55229 18 8 18C7.44772 18 7 17.5523 7 17C7 16.4477 7.44772 16 8 16C8.55229 16 9 16.4477 9 17Z"
                fill="white" />
              <path
                d="M12 18C12.5523 18 13 17.5523 13 17C13 16.4477 12.5523 16 12 16C11.4477 16 11 16.4477 11 17C11 17.5523 11.4477 18 12 18Z"
                fill="white" />
              <path
                d="M13 13C13 13.5523 12.5523 14 12 14C11.4477 14 11 13.5523 11 13C11 12.4477 11.4477 12 12 12C12.5523 12 13 12.4477 13 13Z"
                fill="white" />
              <path
                d="M16 14C16.5523 14 17 13.5523 17 13C17 12.4477 16.5523 12 16 12C15.4477 12 15 12.4477 15 13C15 13.5523 15.4477 14 16 14Z"
                fill="white" />
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M6 0.5C6.27614 0.5 6.5 0.723858 6.5 1V2.72637C6.66345 2.69868 6.83201 2.67452 7.00593 2.65339C8.2688 2.49999 9.87976 2.5 11.965 2.5H12.035C14.1202 2.5 15.7312 2.49999 16.9941 2.65339C17.168 2.67452 17.3365 2.69868 17.5 2.72637V1C17.5 0.723858 17.7239 0.5 18 0.5C18.2761 0.5 18.5 0.723858 18.5 1V2.96349C19.0965 3.15423 19.6138 3.42649 20.072 3.81777C20.2911 4.00489 20.4951 4.20894 20.6822 4.42804C21.3709 5.2344 21.6909 6.22436 21.8466 7.50593C22 8.7688 22 10.3798 22 12.4651V12.5349C22 14.6202 22 16.2312 21.8466 17.4941C21.6909 18.7756 21.3709 19.7656 20.6822 20.572C20.4951 20.7911 20.2911 20.9951 20.072 21.1822C19.2656 21.8709 18.2756 22.1909 16.9941 22.3466C15.7312 22.5 14.1202 22.5 12.0349 22.5H11.9651C9.87978 22.5 8.2688 22.5 7.00593 22.3466C5.72436 22.1909 4.7344 21.8709 3.92804 21.1822C3.70894 20.9951 3.50489 20.7911 3.31777 20.572C2.62907 19.7656 2.30907 18.7756 2.15339 17.4941C1.99999 16.2312 2 14.6202 2 12.535V12.465C2 10.3798 1.99999 8.7688 2.15339 7.50593C2.30907 6.22436 2.62907 5.2344 3.31777 4.42804C3.50489 4.20894 3.70894 4.00489 3.92804 3.81777C4.38616 3.42649 4.90355 3.15423 5.5 2.96349V1C5.5 0.723858 5.72386 0.5 6 0.5ZM17.5 3.7424V5C17.5 5.27614 17.7239 5.5 18 5.5C18.2761 5.5 18.5 5.27614 18.5 5V4.02566C18.8562 4.16964 19.1565 4.35099 19.4225 4.57817C19.6018 4.73127 19.7687 4.89823 19.9218 5.07748C20.4127 5.65225 20.6897 6.38731 20.8378 7.5H3.16219C3.31034 6.38731 3.58727 5.65225 4.07817 5.07748C4.23127 4.89823 4.39823 4.73127 4.57748 4.57817C4.84348 4.35099 5.1438 4.16964 5.5 4.02566V5C5.5 5.27614 5.72386 5.5 6 5.5C6.27614 5.5 6.5 5.27614 6.5 5V3.7424C6.69519 3.70508 6.90348 3.67319 7.12651 3.6461C8.32212 3.50086 9.87251 3.5 12 3.5C14.1275 3.5 15.6779 3.50086 16.8735 3.6461C17.0965 3.67319 17.3048 3.70508 17.5 3.7424ZM3 12.5C3 10.8564 3.00052 9.55724 3.06772 8.5H20.9323C20.9995 9.55724 21 10.8564 21 12.5C21 14.6275 20.9991 16.1779 20.8539 17.3735C20.7101 18.5574 20.4311 19.3262 19.9218 19.9225C19.7687 20.1018 19.6018 20.2687 19.4225 20.4218C18.8262 20.9311 18.0574 21.2101 16.8735 21.3539C15.6779 21.4991 14.1275 21.5 12 21.5C9.87251 21.5 8.32212 21.4991 7.12651 21.3539C5.94255 21.2101 5.17376 20.9311 4.57748 20.4218C4.39823 20.2687 4.23127 20.1018 4.07817 19.9225C3.5689 19.3262 3.28992 18.5574 3.1461 17.3735C3.00086 16.1779 3 14.6275 3 12.5Z"
                fill="white" />
            </svg>

            Fri, Jun 27 - Fri, Jul 4 (7 nights)

          </div>

          <div class="card_next_info">
            <div class="card_next_from">
              $850
            </div>

            <div class="card_next_price_star">
              $450
            </div>

          </div>


        </div>

      </div>

      <div class="card_next imagine_hotel_3">
        <div class="card_next_price">
          <div class="card_next_city_title">
            Concorde De Luxe Resort
          </div>
          <div class="card_next_city_title_2">
            All Inclusive + Flight
          </div>


          <div class="rating_star_group">

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

          </div>

          <div class="avion_container_0">

            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M12 2.5L14.1329 9.06434H21.035L15.4511 13.1213L17.584 19.6857L12 15.6287L6.41604 19.6857L8.54892 13.1213L2.96496 9.06434H9.86712L12 2.5Z"
                stroke="white" />
            </svg>

            8.8/10 Excellent (1,317)

          </div>

          <div class="avion_container">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                stroke="white" />
            </svg>

            Chisinau (RMO) - Antalya (AYT)

          </div>

          <div class="avion_container_2">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M12 2.5C9.23858 2.5 7 4.73858 7 7.5C7 10.2614 9.23858 12.5 12 12.5C14.7614 12.5 17 10.2614 17 7.5C17 4.73858 14.7614 2.5 12 2.5ZM8 7.5C8 5.29086 9.79086 3.5 12 3.5C14.2091 3.5 16 5.29086 16 7.5C16 9.70914 14.2091 11.5 12 11.5C9.79086 11.5 8 9.70914 8 7.5Z"
                fill="white" />
              <path
                d="M4.5 21C4.5 19.2657 5.56191 18.1567 7.08453 17.454C8.62004 16.7453 10.5405 16.5 12 16.5C13.4595 16.5 15.38 16.7453 16.9155 17.454C18.4381 18.1567 19.5 19.2657 19.5 21C19.5 21.2761 19.7239 21.5 20 21.5C20.2761 21.5 20.5 21.2761 20.5 21C20.5 18.7343 19.0619 17.3433 17.3345 16.546C15.62 15.7547 13.5405 15.5 12 15.5C10.4595 15.5 8.37996 15.7547 6.66547 16.546C4.93809 17.3433 3.5 18.7343 3.5 21C3.5 21.2761 3.72386 21.5 4 21.5C4.27614 21.5 4.5 21.2761 4.5 21Z"
                fill="white" />
            </svg>

            per traveler

          </div>

          <div class="avion_container_3">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M8 14C8.55229 14 9 13.5523 9 13C9 12.4477 8.55229 12 8 12C7.44772 12 7 12.4477 7 13C7 13.5523 7.44772 14 8 14Z"
                fill="white" />
              <path
                d="M9 17C9 17.5523 8.55229 18 8 18C7.44772 18 7 17.5523 7 17C7 16.4477 7.44772 16 8 16C8.55229 16 9 16.4477 9 17Z"
                fill="white" />
              <path
                d="M12 18C12.5523 18 13 17.5523 13 17C13 16.4477 12.5523 16 12 16C11.4477 16 11 16.4477 11 17C11 17.5523 11.4477 18 12 18Z"
                fill="white" />
              <path
                d="M13 13C13 13.5523 12.5523 14 12 14C11.4477 14 11 13.5523 11 13C11 12.4477 11.4477 12 12 12C12.5523 12 13 12.4477 13 13Z"
                fill="white" />
              <path
                d="M16 14C16.5523 14 17 13.5523 17 13C17 12.4477 16.5523 12 16 12C15.4477 12 15 12.4477 15 13C15 13.5523 15.4477 14 16 14Z"
                fill="white" />
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M6 0.5C6.27614 0.5 6.5 0.723858 6.5 1V2.72637C6.66345 2.69868 6.83201 2.67452 7.00593 2.65339C8.2688 2.49999 9.87976 2.5 11.965 2.5H12.035C14.1202 2.5 15.7312 2.49999 16.9941 2.65339C17.168 2.67452 17.3365 2.69868 17.5 2.72637V1C17.5 0.723858 17.7239 0.5 18 0.5C18.2761 0.5 18.5 0.723858 18.5 1V2.96349C19.0965 3.15423 19.6138 3.42649 20.072 3.81777C20.2911 4.00489 20.4951 4.20894 20.6822 4.42804C21.3709 5.2344 21.6909 6.22436 21.8466 7.50593C22 8.7688 22 10.3798 22 12.4651V12.5349C22 14.6202 22 16.2312 21.8466 17.4941C21.6909 18.7756 21.3709 19.7656 20.6822 20.572C20.4951 20.7911 20.2911 20.9951 20.072 21.1822C19.2656 21.8709 18.2756 22.1909 16.9941 22.3466C15.7312 22.5 14.1202 22.5 12.0349 22.5H11.9651C9.87978 22.5 8.2688 22.5 7.00593 22.3466C5.72436 22.1909 4.7344 21.8709 3.92804 21.1822C3.70894 20.9951 3.50489 20.7911 3.31777 20.572C2.62907 19.7656 2.30907 18.7756 2.15339 17.4941C1.99999 16.2312 2 14.6202 2 12.535V12.465C2 10.3798 1.99999 8.7688 2.15339 7.50593C2.30907 6.22436 2.62907 5.2344 3.31777 4.42804C3.50489 4.20894 3.70894 4.00489 3.92804 3.81777C4.38616 3.42649 4.90355 3.15423 5.5 2.96349V1C5.5 0.723858 5.72386 0.5 6 0.5ZM17.5 3.7424V5C17.5 5.27614 17.7239 5.5 18 5.5C18.2761 5.5 18.5 5.27614 18.5 5V4.02566C18.8562 4.16964 19.1565 4.35099 19.4225 4.57817C19.6018 4.73127 19.7687 4.89823 19.9218 5.07748C20.4127 5.65225 20.6897 6.38731 20.8378 7.5H3.16219C3.31034 6.38731 3.58727 5.65225 4.07817 5.07748C4.23127 4.89823 4.39823 4.73127 4.57748 4.57817C4.84348 4.35099 5.1438 4.16964 5.5 4.02566V5C5.5 5.27614 5.72386 5.5 6 5.5C6.27614 5.5 6.5 5.27614 6.5 5V3.7424C6.69519 3.70508 6.90348 3.67319 7.12651 3.6461C8.32212 3.50086 9.87251 3.5 12 3.5C14.1275 3.5 15.6779 3.50086 16.8735 3.6461C17.0965 3.67319 17.3048 3.70508 17.5 3.7424ZM3 12.5C3 10.8564 3.00052 9.55724 3.06772 8.5H20.9323C20.9995 9.55724 21 10.8564 21 12.5C21 14.6275 20.9991 16.1779 20.8539 17.3735C20.7101 18.5574 20.4311 19.3262 19.9218 19.9225C19.7687 20.1018 19.6018 20.2687 19.4225 20.4218C18.8262 20.9311 18.0574 21.2101 16.8735 21.3539C15.6779 21.4991 14.1275 21.5 12 21.5C9.87251 21.5 8.32212 21.4991 7.12651 21.3539C5.94255 21.2101 5.17376 20.9311 4.57748 20.4218C4.39823 20.2687 4.23127 20.1018 4.07817 19.9225C3.5689 19.3262 3.28992 18.5574 3.1461 17.3735C3.00086 16.1779 3 14.6275 3 12.5Z"
                fill="white" />
            </svg>

            Fri, Jun 27 - Fri, Jul 4 (7 nights)

          </div>

          <div class="card_next_info">
            <div class="card_next_from">
              $850
            </div>

            <div class="card_next_price_star">
              $450
            </div>

          </div>


        </div>

      </div>

      <div class="card_next imagine_hotel_4">
        <div class="card_next_price">
          <div class="card_next_city_title">
            Concorde De Luxe Resort
          </div>
          <div class="card_next_city_title_2">
            All Inclusive + Flight
          </div>


          <div class="rating_star_group">

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="15" viewBox="0 0 16 15" fill="none">
              <path
                d="M8 0L9.79611 5.52786H15.6085L10.9062 8.94427L12.7023 14.4721L8 11.0557L3.29772 14.4721L5.09383 8.94427L0.391548 5.52786H6.20389L8 0Z"
                fill="#FFC084" />
            </svg>

          </div>

          <div class="avion_container_0">

            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M12 2.5L14.1329 9.06434H21.035L15.4511 13.1213L17.584 19.6857L12 15.6287L6.41604 19.6857L8.54892 13.1213L2.96496 9.06434H9.86712L12 2.5Z"
                stroke="white" />
            </svg>

            8.8/10 Excellent (1,317)

          </div>

          <div class="avion_container">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                stroke="white" />
            </svg>

            Chisinau (RMO) - Antalya (AYT)

          </div>

          <div class="avion_container_2">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M12 2.5C9.23858 2.5 7 4.73858 7 7.5C7 10.2614 9.23858 12.5 12 12.5C14.7614 12.5 17 10.2614 17 7.5C17 4.73858 14.7614 2.5 12 2.5ZM8 7.5C8 5.29086 9.79086 3.5 12 3.5C14.2091 3.5 16 5.29086 16 7.5C16 9.70914 14.2091 11.5 12 11.5C9.79086 11.5 8 9.70914 8 7.5Z"
                fill="white" />
              <path
                d="M4.5 21C4.5 19.2657 5.56191 18.1567 7.08453 17.454C8.62004 16.7453 10.5405 16.5 12 16.5C13.4595 16.5 15.38 16.7453 16.9155 17.454C18.4381 18.1567 19.5 19.2657 19.5 21C19.5 21.2761 19.7239 21.5 20 21.5C20.2761 21.5 20.5 21.2761 20.5 21C20.5 18.7343 19.0619 17.3433 17.3345 16.546C15.62 15.7547 13.5405 15.5 12 15.5C10.4595 15.5 8.37996 15.7547 6.66547 16.546C4.93809 17.3433 3.5 18.7343 3.5 21C3.5 21.2761 3.72386 21.5 4 21.5C4.27614 21.5 4.5 21.2761 4.5 21Z"
                fill="white" />
            </svg>

            per traveler

          </div>

          <div class="avion_container_3">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M8 14C8.55229 14 9 13.5523 9 13C9 12.4477 8.55229 12 8 12C7.44772 12 7 12.4477 7 13C7 13.5523 7.44772 14 8 14Z"
                fill="white" />
              <path
                d="M9 17C9 17.5523 8.55229 18 8 18C7.44772 18 7 17.5523 7 17C7 16.4477 7.44772 16 8 16C8.55229 16 9 16.4477 9 17Z"
                fill="white" />
              <path
                d="M12 18C12.5523 18 13 17.5523 13 17C13 16.4477 12.5523 16 12 16C11.4477 16 11 16.4477 11 17C11 17.5523 11.4477 18 12 18Z"
                fill="white" />
              <path
                d="M13 13C13 13.5523 12.5523 14 12 14C11.4477 14 11 13.5523 11 13C11 12.4477 11.4477 12 12 12C12.5523 12 13 12.4477 13 13Z"
                fill="white" />
              <path
                d="M16 14C16.5523 14 17 13.5523 17 13C17 12.4477 16.5523 12 16 12C15.4477 12 15 12.4477 15 13C15 13.5523 15.4477 14 16 14Z"
                fill="white" />
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M6 0.5C6.27614 0.5 6.5 0.723858 6.5 1V2.72637C6.66345 2.69868 6.83201 2.67452 7.00593 2.65339C8.2688 2.49999 9.87976 2.5 11.965 2.5H12.035C14.1202 2.5 15.7312 2.49999 16.9941 2.65339C17.168 2.67452 17.3365 2.69868 17.5 2.72637V1C17.5 0.723858 17.7239 0.5 18 0.5C18.2761 0.5 18.5 0.723858 18.5 1V2.96349C19.0965 3.15423 19.6138 3.42649 20.072 3.81777C20.2911 4.00489 20.4951 4.20894 20.6822 4.42804C21.3709 5.2344 21.6909 6.22436 21.8466 7.50593C22 8.7688 22 10.3798 22 12.4651V12.5349C22 14.6202 22 16.2312 21.8466 17.4941C21.6909 18.7756 21.3709 19.7656 20.6822 20.572C20.4951 20.7911 20.2911 20.9951 20.072 21.1822C19.2656 21.8709 18.2756 22.1909 16.9941 22.3466C15.7312 22.5 14.1202 22.5 12.0349 22.5H11.9651C9.87978 22.5 8.2688 22.5 7.00593 22.3466C5.72436 22.1909 4.7344 21.8709 3.92804 21.1822C3.70894 20.9951 3.50489 20.7911 3.31777 20.572C2.62907 19.7656 2.30907 18.7756 2.15339 17.4941C1.99999 16.2312 2 14.6202 2 12.535V12.465C2 10.3798 1.99999 8.7688 2.15339 7.50593C2.30907 6.22436 2.62907 5.2344 3.31777 4.42804C3.50489 4.20894 3.70894 4.00489 3.92804 3.81777C4.38616 3.42649 4.90355 3.15423 5.5 2.96349V1C5.5 0.723858 5.72386 0.5 6 0.5ZM17.5 3.7424V5C17.5 5.27614 17.7239 5.5 18 5.5C18.2761 5.5 18.5 5.27614 18.5 5V4.02566C18.8562 4.16964 19.1565 4.35099 19.4225 4.57817C19.6018 4.73127 19.7687 4.89823 19.9218 5.07748C20.4127 5.65225 20.6897 6.38731 20.8378 7.5H3.16219C3.31034 6.38731 3.58727 5.65225 4.07817 5.07748C4.23127 4.89823 4.39823 4.73127 4.57748 4.57817C4.84348 4.35099 5.1438 4.16964 5.5 4.02566V5C5.5 5.27614 5.72386 5.5 6 5.5C6.27614 5.5 6.5 5.27614 6.5 5V3.7424C6.69519 3.70508 6.90348 3.67319 7.12651 3.6461C8.32212 3.50086 9.87251 3.5 12 3.5C14.1275 3.5 15.6779 3.50086 16.8735 3.6461C17.0965 3.67319 17.3048 3.70508 17.5 3.7424ZM3 12.5C3 10.8564 3.00052 9.55724 3.06772 8.5H20.9323C20.9995 9.55724 21 10.8564 21 12.5C21 14.6275 20.9991 16.1779 20.8539 17.3735C20.7101 18.5574 20.4311 19.3262 19.9218 19.9225C19.7687 20.1018 19.6018 20.2687 19.4225 20.4218C18.8262 20.9311 18.0574 21.2101 16.8735 21.3539C15.6779 21.4991 14.1275 21.5 12 21.5C9.87251 21.5 8.32212 21.4991 7.12651 21.3539C5.94255 21.2101 5.17376 20.9311 4.57748 20.4218C4.39823 20.2687 4.23127 20.1018 4.07817 19.9225C3.5689 19.3262 3.28992 18.5574 3.1461 17.3735C3.00086 16.1779 3 14.6275 3 12.5Z"
                fill="white" />
            </svg>

            Fri, Jun 27 - Fri, Jul 4 (7 nights)

          </div>

          <div class="card_next_info">
            <div class="card_next_from">
              $850
            </div>

            <div class="card_next_price_star">
              $450
            </div>

          </div>


        </div>

      </div>



    </div>
  </div>

  <!-- <div class="parent">
    <div class="text">
      This is a long piece of text that should be truncated with ellipsis if it overflows.
    </div>
  </div> -->


</template>

<style scoped>
/* .parent {
  display: flex;
  width: 200px;
  border: 1px solid #ccc;
}

.text {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  flex: 1;
} */

.next_component {
  margin-top: 280px;
  display: flex;
  flex-direction: column;
  gap: 56px;
}

.titlu_taburi {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 32px;
}

.titlu_inspiration {
  color: #000;
  font-family: Jost;
  font-size: 48px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

/* taburile */

.containerul_taburi {
  display: flex;
  height: 44px;
  justify-content: center;
  align-items: flex-end;
  gap: 32px;
}

.tab_elemet {

  display: flex;
  padding: 12px 0px;
  justify-content: center;
  align-items: center;

  position: relative;

  cursor: pointer;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.tab_label {
  color: rgba(0, 0, 0, 0.56);
  text-overflow: ellipsis;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 16px;
  /* 100% */
  letter-spacing: 0.64px;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.tab_elemet:hover .tab_label {
  transform: translateY(-4px);
}


.linie_tab {
  position: absolute;
  top: 96%;
  width: 100%;
  height: 1px;
  background-color: #000;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.tab_elemet:hover .linie_tab {

  transform: scaleX(0.5);

}

.label_default {
  color: rgba(0, 0, 0, 1);
}

.linie_tab_default {
  position: absolute;
  top: 96%;
  width: 100%;
  height: 1px;
  background-color: #000;

  transform: scaleX(1);
  opacity: 0;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.tab_elemet:hover .linie_tab_default {

  transform: scaleX(0.5);
  opacity: 0.16;

}

/* cardurile */

.next_group {
  display: flex;
  padding: 0px 132px;
  align-items: center;
  gap: 40px;
}

.card_next {
  height: 694px;
  flex: 1 0 0;

  border-radius: 48px;

  cursor: pointer;
  transition: flex 1000ms cubic-bezier(0.3, 0, 0, 1);

  position: relative;

  display: flex;
}

.card_next:hover {
  flex: 3 0 0;
}

.imagine_hotel_1 {
  background: url(/src/components/media/hotel_1.jpg) lightgray 50% / cover no-repeat;
}

.imagine_hotel_2 {
  background: url(/src/components/media/hotel_2.jpg) lightgray 50% / cover no-repeat;
}

.imagine_hotel_3 {
  background: url(/src/components/media/hotel_3.jpg) lightgray 50% / cover no-repeat;
}

.imagine_hotel_4 {
  background: url(/src/components/media/hotel_4.jpg) lightgray 50% / cover no-repeat;
}

.card_next_price {

  flex: 1 0 0;

  display: flex;
  padding: 16px 8px 24px 8px;
  flex-direction: column;
  align-items: center;
  gap: 12px;

  margin: 16px;
  margin-top: 488px;

  border-radius: 32px;
  background: rgba(104, 97, 155, 0.08);
  backdrop-filter: blur(16px);

  transition: all 1000ms cubic-bezier(0.3, 0, 0, 1);
  position: relative;

}

.card_next:hover .card_next_price {
  margin-top: 460px;
}

.avion_container_0 {
  display: flex;
  align-items: center;
  gap: 8px;

  color: #FFF;
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 16px;
  /* 100% */
  letter-spacing: 0.64px;

  position: absolute;

  top: 76px;
  left: 124px;
  opacity: 0;

  transition: all 1000ms cubic-bezier(0.3, 0, 0, 1);

}

.card_next:hover .avion_container_0 {
  top: 60px;
  left: 32px;
  opacity: 1;
}

.avion_container {
  display: flex;
  align-items: center;
  gap: 8px;

  color: #FFF;
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 16px;
  /* 100% */
  letter-spacing: 0.64px;

  position: absolute;

  top: 96px;
  left: 124px;
  opacity: 0;

  transition: all 1000ms cubic-bezier(0.3, 0, 0, 1);

}

.card_next:hover .avion_container {
  top: 96px;
  left: 32px;
  opacity: 1;
}

.avion_container_2 {
  display: flex;
  align-items: center;
  gap: 8px;

  color: #FFF;
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 16px;
  /* 100% */
  letter-spacing: 0.64px;

  position: absolute;

  top: 116px;
  left: 124px;
  opacity: 0;

  transition: all 1000ms cubic-bezier(0.3, 0, 0, 1);

}

.card_next:hover .avion_container_2 {
  top: 132px;
  left: 32px;
  opacity: 1;
}

.avion_container_3 {
  display: flex;
  align-items: center;
  gap: 8px;

  color: #FFF;
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 16px;
  /* 100% */
  letter-spacing: 0.64px;

  position: absolute;

  top: 136px;
  left: 124px;
  opacity: 0;

  transition: all 1000ms cubic-bezier(0.3, 0, 0, 1);

}

.card_next:hover .avion_container_3 {
  top: 168px;
  left: 32px;
  opacity: 1;
}

/* .hotel_name {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
} */

.card_next_city_title {
  color: #FFF;
  text-align: center;
  font-family: Jost;
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 32px;

  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;

  position: absolute;
  left: 50%;
  top: 16px;
  transform: translateX(-50%);

  width: calc(100% - 32px);
  /* leave space for padding (8px left/right + margin) */

  transition: all 1000ms cubic-bezier(0.3, 0, 0, 1);
}

.card_next:hover .card_next_city_title {
  width: 260px;
  left: 32px;
  top: 16px;
  transform: translateX(0%);
}

.card_next_city_title_2 {
  color: #FFF;
  text-align: center;
  font-family: Jost;
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 32px;
  /* 133.333% */

  white-space: nowrap;

  position: absolute;
  right: 50%;
  top: 48px;
  transform: translateX(50%);

  transition: all 1000ms cubic-bezier(0.3, 0, 0, 1);
}

.card_next:hover .card_next_city_title_2 {
  right: 32px;
  top: 16px;
  transform: translateX(0%);
}

.rating_star_group {
  display: flex;
  align-items: flex-start;
  gap: 8px;

  position: absolute;
  left: 50%;
  top: 92px;
  transform: translateX(-50%);

  transition: all 1000ms cubic-bezier(0.3, 0, 0, 1);
}

.card_next:hover .rating_star_group {
  left: 24px;
  top: 60px;
  transform: translateX(0%);
  opacity: 0;
}

.card_next_info {
  display: flex;
  justify-content: flex-end;
  align-items: baseline;
  gap: 8px;

  position: absolute;
  right: 54%;
  bottom: 24px;
  transform: translateX(50%);

  transition: all 1000ms cubic-bezier(0.3, 0, 0, 1);
}



.card_next:hover .card_next_info {
  right: 32px;
  bottom: 24px;
  transform: translateX(0%);
}

.card_next_from {
  color: rgba(255, 255, 255, 0.48);
  text-align: center;
  font-family: Jost;
  font-size: 20px;
  font-style: normal;
  font-weight: 300;
  line-height: normal;

  display: flex;
  padding-top: 2px;
  align-items: flex-start;
  gap: 8px;
  text-decoration-line: line-through;
}

.card_next_price_star {
  color: #FFF;
  text-align: center;
  font-family: Jost;
  font-size: 32px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;

  display: flex;
  align-items: flex-start;
  gap: 2px;
}
</style>
