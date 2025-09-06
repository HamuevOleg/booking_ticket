<script setup>

// ====== Importare biblioteca paralax ======

import { gsap, } from "gsap"
import { ScrollTrigger } from "gsap/ScrollTrigger"
import { onMounted } from "vue"

gsap.registerPlugin(ScrollTrigger)


onMounted(() => {

  gsap.from(".map_title_parallax", {
    scrollTrigger: {
      trigger: ".map_component",
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

  gsap.from(".map_card", {
    scrollTrigger: {
      trigger: ".map_component",
      start: "top 80%",
      end: "top 30%",
      // markers: true,
      scrub: true
    },
    ease: "power2inOut",
    opacity: 0,
    stagger: 0.2,
  })

  gsap.from(".map_point_parallax", {
    scrollTrigger: {
      trigger: ".map_graph_container",
      start: "top 80%",
      end: "top 30%",
      // markers: true,
      scrub: true
    },
    y: 64,
    ease: "power2inOut",
    opacity: 0,
    scale: 0.6,
    stagger: 0.2,
  })


})


</script>

<template>
  <div class="map_component">

    <div class="map_mainj_title map_title_parallax">
      Find the flights on the map
    </div>

    <div class="map_tab_container map_title_parallax">

      <div class="radio_element">
        <div class="map_radio_up">
          <div class="map_radio_deep">
          </div>
        </div>

        Any number of stops
      </div>

      <div class="radio_element">
        <div class="map_radio_up_selected">
          <div class="map_radio_deep_selected">
          </div>
        </div>

        Nonstop only
      </div>

      <div class="radio_element">
        <div class="map_radio_up">
          <div class="map_radio_deep">
          </div>
        </div>

        One stop or fewer
      </div>

      <div class="radio_element">
        <div class="map_radio_up">
          <div class="map_radio_deep">
          </div>
        </div>

        Two stops or fewer
      </div>



    </div>

    <div class="map_card_group">

      <div class="map_card">

        <div class="card_title">

          <svg xmlns="http://www.w3.org/2000/svg" width="28" height="20" viewBox="0 0 28 20" fill="none">
            <rect x="0.25" y="0.25" width="27.5" height="19.5" rx="1.75" fill="white" stroke="#E0E0E0"
              stroke-width="0.5" />
            <mask id="mask0_812_9840" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="0" y="0" width="28"
              height="20">
              <rect width="28" height="20" rx="2" fill="white" />
            </mask>
            <g mask="url(#mask0_812_9840)">
              <rect x="18.667" width="9.33333" height="20" fill="#E43D4C" />
              <path fill-rule="evenodd" clip-rule="evenodd" d="M0 20H9.33333V0H0V20Z" fill="#1BB65D" />
            </g>
          </svg>

          <div class="card_title_main">
            Italy
          </div>

          <div class="card_title_race">
            20 routes
          </div>

        </div>

        <div class="card_price">
          $450
        </div>

      </div>

      <div class="map_card">

        <div class="card_title">

          <svg xmlns="http://www.w3.org/2000/svg" width="28" height="20" viewBox="0 0 28 20" fill="none">
            <rect x="0.25" y="0.25" width="27.5" height="19.5" rx="1.75" fill="white" stroke="#F5F5F5"
              stroke-width="0.5" />
            <mask id="mask0_812_9848" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="0" y="0" width="28"
              height="20">
              <rect x="0.25" y="0.25" width="27.5" height="19.5" rx="1.75" fill="white" stroke="white"
                stroke-width="0.5" />
            </mask>
            <g mask="url(#mask0_812_9848)">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M0 6.66667H28V0H0V6.66667Z" fill="#E03D52" />
              <path fill-rule="evenodd" clip-rule="evenodd" d="M0 19.9997H28V13.333H0V19.9997Z" fill="#5A9165" />
            </g>
          </svg>

          <div class="card_title_main">
            Hungary
          </div>

          <div class="card_title_race">
            3 routes
          </div>

        </div>

        <div class="card_price">
          $250
        </div>

      </div>

      <div class="map_card">

        <div class="card_title">

          <svg xmlns="http://www.w3.org/2000/svg" width="28" height="20" viewBox="0 0 28 20" fill="none">
            <rect width="28" height="20" rx="2" fill="white" />
            <mask id="mask0_812_9858" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="0" y="0" width="28"
              height="20">
              <rect width="28" height="20" rx="2" fill="white" />
            </mask>
            <g mask="url(#mask0_812_9858)">
              <rect x="13.333" width="14.6667" height="20" fill="#E5253D" />
              <path fill-rule="evenodd" clip-rule="evenodd" d="M0 20H9.33333V0H0V20Z" fill="#0A3D9C" />
              <path fill-rule="evenodd" clip-rule="evenodd" d="M9.33301 20H18.6663V0H9.33301V20Z" fill="#FFD955" />
            </g>
          </svg>

          <div class="card_title_main">
            Romania
          </div>

          <div class="card_title_race">
            12 routes
          </div>

        </div>

        <div class="card_price">
          $120
        </div>

      </div>

      <div class="map_card">

        <div class="card_title">

          <svg xmlns="http://www.w3.org/2000/svg" width="28" height="20" viewBox="0 0 28 20" fill="none">
            <rect x="0.25" y="0.25" width="27.5" height="19.5" rx="1.75" fill="white" stroke="#E0E0E0"
              stroke-width="0.5" />
            <mask id="mask0_812_9868" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="0" y="0" width="28"
              height="20">
              <rect width="28" height="20" rx="2" fill="white" />
            </mask>
            <g mask="url(#mask0_812_9868)">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M0 19.9997H28V9.33301H0V19.9997Z" fill="#EB2A50" />
            </g>
          </svg>

          <div class="card_title_main">
            Poland
          </div>

          <div class="card_title_race">
            6 routes
          </div>

        </div>

        <div class="card_price">
          $150
        </div>

      </div>

      <div class="map_card">

        <div class="card_title">

          <svg xmlns="http://www.w3.org/2000/svg" width="28" height="20" viewBox="0 0 28 20" fill="none">
            <rect width="28" height="20" rx="2" fill="white" />
            <mask id="mask0_812_9878" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="0" y="0" width="28"
              height="20">
              <rect width="28" height="20" rx="2" fill="white" />
            </mask>
            <g mask="url(#mask0_812_9878)">
              <rect width="28" height="20" fill="#0A17A7" />
              <path
                d="M30.7734 0.294922L21.3262 6.66699H28V13.334H21.3262L30.7734 19.7061L29.2822 21.917L17.334 13.8574V21.334H10.667V13.8564L-1.28223 21.917L-2.77344 19.7061L6.67383 13.334H0V6.66699H6.67383L-2.77344 0.294922L-1.28223 -1.91602L10.667 6.14355V-1.33301H17.334V6.14258L29.2822 -1.91602L30.7734 0.294922Z"
                fill="white" />
              <path d="M18.668 6.33219L31.3333 -2" stroke="#DB1F35" stroke-width="0.666667" stroke-linecap="round" />
              <path d="M20.0127 13.6978L31.3665 21.3506" stroke="#DB1F35" stroke-width="0.666667"
                stroke-linecap="round" />
              <path d="M8.00562 6.31055L-3.8374 -1.6709" stroke="#DB1F35" stroke-width="0.666667"
                stroke-linecap="round" />
              <path d="M9.29012 13.605L-3.8374 22.3105" stroke="#DB1F35" stroke-width="0.666667"
                stroke-linecap="round" />
              <path fill-rule="evenodd" clip-rule="evenodd" d="M0 12H12V20H16V12H28V8H16V0H12V8H0V12Z" fill="#E6273E" />
            </g>
          </svg>

          <div class="card_title_main">
            UK
          </div>

          <div class="card_title_race">
            3 routes
          </div>

        </div>

        <div class="card_price">
          $650
        </div>

      </div>

      <div class="map_card_button">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
          <path d="M8.25 4.5L15.6439 11.8939C15.7025 11.9525 15.7025 12.0475 15.6439 12.1061L8.25 19.5" stroke="#816EFC"
            stroke-width="2.25" stroke-linecap="round" />
        </svg>
      </div>

    </div>

    <div class="map_graph_container">

      <div class="map_flight_card_london map_point_parallax">
        <div class="map_flight_card">
          <div class="flight_details">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="#816EFC" />
            </svg>

            <div class="flight_details_info">
              <div class="details_info_title">
                London
              </div>

              <div class="details_info_price">
                $850
              </div>

            </div>
          </div>
          <div class="map_flight_point"></div>

        </div>


      </div>

      <div class="map_point_from map_point_parallax">

        <div class="from_card">

          <div class="from_details">
            <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="none">
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M16 30C16 30 26 19.1405 26 12.2222C26 6.57665 21.5228 2 16 2C10.4772 2 6 6.57665 6 12.2222C6 19.1405 16 30 16 30ZM16 16C18.0711 16 19.75 14.2905 19.75 12.1818C19.75 10.0731 18.0711 8.36364 16 8.36364C13.9289 8.36364 12.25 10.0731 12.25 12.1818C12.25 14.2905 13.9289 16 16 16Z"
                fill="#816EFC" />
            </svg>
            Chișinău
          </div>

          <div class="from_point"></div>

        </div>
      </div>

      <div class="map_flight_card_berlin map_point_parallax">
        <div class="map_flight_card">
          <div class="flight_details">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="#816EFC" />
            </svg>

            <div class="flight_details_info">
              <div class="details_info_title">
                Berlin
              </div>

              <div class="details_info_price">
                $220
              </div>

            </div>
          </div>
          <div class="map_flight_point"></div>

        </div>


      </div>

      <div class="map_flight_card_warsaw map_point_parallax">
        <div class="map_flight_card">
          <div class="flight_details">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="#816EFC" />
            </svg>

            <div class="flight_details_info">
              <div class="details_info_title">
                Warsaw
              </div>

              <div class="details_info_price">
                $150
              </div>

            </div>
          </div>
          <div class="map_flight_point"></div>

        </div>


      </div>

      <div class="map_flight_card_paris map_point_parallax">
        <div class="map_flight_card">
          <div class="flight_details">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="#816EFC" />
            </svg>

            <div class="flight_details_info">
              <div class="details_info_title">
                Paris
              </div>

              <div class="details_info_price">
                $600
              </div>

            </div>
          </div>
          <div class="map_flight_point"></div>

        </div>


      </div>

      <div class="map_flight_card_budapest map_point_parallax">
        <div class="map_flight_card">
          <div class="flight_details">

            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="#816EFC" />
            </svg>

            <div class="flight_details_info">
              <div class="details_info_title">
                Budapest
              </div>

              <div class="details_info_price">
                $120
              </div>

            </div>
          </div>
          <div class="map_flight_point"></div>

        </div>


      </div>

      <div class="map_flight_card_bucharest map_point_parallax">
        <div class="map_flight_card">
          <div class="flight_details">

            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="#816EFC" />
            </svg>

            <div class="flight_details_info">
              <div class="details_info_title">
                Bucharest
              </div>

              <div class="details_info_price">
                $90
              </div>

            </div>
          </div>
          <div class="map_flight_point"></div>

        </div>


      </div>

      <div class="map_flight_card_rome map_point_parallax">
        <div class="map_flight_card">
          <div class="flight_details">

            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="#816EFC" />
            </svg>

            <div class="flight_details_info">
              <div class="details_info_title">
                Rome
              </div>

              <div class="details_info_price">
                $480
              </div>

            </div>
          </div>
          <div class="map_flight_point"></div>

        </div>


      </div>

      <div class="map_flight_card_barcelona map_point_parallax">
        <div class="map_flight_card">
          <div class="flight_details">

            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="#816EFC" />
            </svg>

            <div class="flight_details_info">
              <div class="details_info_title">
                Barcelona
              </div>

              <div class="details_info_price">
                $480
              </div>

            </div>
          </div>
          <div class="map_flight_point"></div>

        </div>


      </div>

      <div class="group_butoane_map">
        <div class="button_map">

          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
            <path class="button_icon_stroke" d="M4 12H20" stroke-width="2.25" stroke-linecap="round" />
            <path class="button_icon_stroke" d="M12 20L12 4" stroke-width="2.25" stroke-linecap="round" />
          </svg>

        </div>

        <div class="button_map">

          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
            <path class="button_icon_stroke" d="M4 12H20" stroke-opacity="0.64" stroke-width="2.25"
              stroke-linecap="round" />
          </svg>

        </div>


      </div>

    </div>



  </div>


</template>

<style scoped>
.map_component {
  margin-top: 280px;
  display: flex;
  flex-direction: column;
  padding: 0px 132px;
  align-items: center;
  gap: 48px;
  align-self: stretch;
}

.map_mainj_title {
  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 32px;
  font-style: normal;
  font-weight: 500;
  line-height: 40px;
  /* 125% */
}

.map_tab_container {
  display: flex;
  align-items: center;
  gap: 40px;
}

.radio_element {
  display: flex;
  align-items: center;
  gap: 8px;

  color: #000;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 16px;
  /* 100% */
  letter-spacing: 0.64px;

  cursor: pointer;
}

.map_radio_up {
  display: flex;
  width: 16px;
  height: 16px;
  padding: 6px;
  align-items: center;
  gap: 10px;

  border-radius: 14px;
  border: 1px solid rgba(0, 0, 0, 0.16);

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.radio_element:hover .map_radio_up {
  border: 1px solid rgba(129, 110, 252, 0.64);
}

.map_radio_deep {
  width: 16px;
  height: 16px;
  flex-shrink: 0;

  border-radius: 14px;
  background: rgba(0, 0, 0, 0.00);
  transform: scale(0.8);
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.radio_element:hover .map_radio_deep {
  transform: scale(1.2);
  background: rgba(129, 110, 252, 0.16);
}

.map_radio_up_selected {
  display: flex;
  width: 16px;
  height: 16px;
  padding: 6px;
  align-items: center;
  gap: 10px;

  border-radius: 14px;
  border: 1px solid #816EFC;
}

.map_radio_deep_selected {
  width: 16px;
  height: 16px;
  flex-shrink: 0;

  border-radius: 14px;
  background: #816EFC;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.radio_element:hover .map_radio_deep_selected {
  transform: scale(1.2);
}

.map_card_group {
  display: flex;
  align-items: center;
  gap: 24px;
  align-self: stretch;
}

.map_card {
  display: flex;
  padding: 20px;
  justify-content: space-between;
  align-items: center;
  flex: 1 0 0;

  border-radius: 20px;
  background: #FFF;
  box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.08);

  cursor: pointer;
  transition: shadow 400ms cubic-bezier(0.3, 0, 0, 1),
    transform 400ms cubic-bezier(0.3, 0, 0, 1);
}

.map_card:hover {
  box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.08);
  transform: translateY(-6px);
}

.map_card_button {
  display: flex;
  padding: 20px;
  align-items: center;
  gap: 64px;
  border-radius: 20px;
  background: #FFF;
  box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.08);

  cursor: pointer;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.map_card_button:hover {
  box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.08);
  transform: translateY(-6px);
}

.card_title {
  display: flex;
  align-items: center;
  gap: 12px;
}

.card_title_main {
  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: 24px;
  /* 150% */
}

.card_title_race {
  color: rgba(0, 0, 0, 0.72);
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  /* 150% */
}

.card_price {
  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 24px;
  /* 120% */
}

.map_graph_container {
  display: flex;
  width: 100%;
  height: 680px;
  justify-content: space-between;
  align-items: center;

  border-radius: 40px;
  border: 1px solid rgba(33, 0, 93, 0.08);
  background: #FFF;
  box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.08);

  background: url(/src/components/media/map_avia.svg) rgb(255, 255, 255) 70% 70% no-repeat;

  position: relative;
}

.map_flight_card_london {
  position: absolute;
  top: 106px;
  left: 28%;
}

.map_flight_card_berlin {
  position: absolute;
  top: 54px;
  left: 49%;
}

.map_flight_card_warsaw {
  position: absolute;
  top: 76px;
  left: 60%;
}

.map_flight_card_paris {
  position: absolute;
  top: 206px;
  left: 32%;
}

.map_flight_card_budapest {
  position: absolute;
  top: 268px;
  left: 57%;
}

.map_flight_card_bucharest {
  position: absolute;
  top: 370px;
  left: 67%;
}

.map_flight_card_rome {
  position: absolute;
  top: 460px;
  left: 48%;
}

.map_flight_card_barcelona {
  position: absolute;
  top: 472px;
  left: 31%;
}


.map_flight_card {
  display: flex;
  /* width: 110px; */
  height: 68px;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  flex-shrink: 0;

  cursor: pointer;

}


.map_flight_point {
  width: 8px;
  height: 8px;
  flex-shrink: 0;

  border-radius: 8px;
  background: #816EFC;
}

.flight_details {
  display: flex;
  padding: 8px 24px 8px 16px;
  justify-content: center;
  align-items: center;
  gap: 8px;
  align-self: stretch;

  border-radius: 16px;
  background: rgba(255, 255, 255, 0.90);
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.map_flight_card:hover .flight_details {
  transform: translateY(-8px);
}

.flight_details_info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  gap: 4px;
}

.details_info_title {
  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 16px;
  /* 114.286% */
  letter-spacing: 0.56px;
}

.details_info_price {
  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: 16px;
  /* 114.286% */
  letter-spacing: 0.56px;
}

.map_point_from {
  position: absolute;
  top: 279px;
  left: 74%;
}

.from_card {
  display: flex;

  height: 64px;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  flex-shrink: 0;

  position: relative;
}

.from_details {
  display: flex;
  padding: 8px 16px;
  justify-content: center;
  align-items: center;
  gap: 8px;
  align-self: stretch;

  border-radius: 16px;
  background: rgba(255, 255, 255, 0.90);

  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: 16px;
  /* 114.286% */
  letter-spacing: 0.56px;
}

.from_point {
  border-radius: 8px;
  background: #816EFC;
  width: 8px;
  height: 8px;
  position: absolute;
  left: 27px;
  bottom: 0px;
}

.group_butoane_map {
  display: flex;
  width: 40px;
  flex-direction: column;
  align-items: flex-start;
  gap: 8px;

  position: absolute;
  right: 24px;
  top: 24px;
}

.button_map {
  display: flex;
  padding: 8px;
  align-items: center;
  gap: 64px;
  align-self: stretch;

  border-radius: 12px;
  background: #FFF;
  box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.08);

  cursor: pointer;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.button_map:hover {
  box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.08);
}

.button_icon_stroke {
  stroke: #000000;
  stroke-opacity: 0.64;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.button_map:hover .button_icon_stroke {
  stroke: #816EFC;
  stroke-opacity: 0.48;
}
</style>
