<script setup>

// ====== Importare biblioteca paralax ======

import { gsap } from "gsap"
import { ScrollTrigger } from "gsap/ScrollTrigger"
import { onMounted } from "vue"

gsap.registerPlugin(ScrollTrigger)


onMounted(() => {

  gsap.from(".group_para", {
    scrollTrigger: {
      trigger: ".ceo_scroll_group",
      start: "20% bottom",
      end: "130% bottom",
      // markers: true,
      scrub: true,
      // toggleActions: "restart pause reverse pause"
    },
    y: 32,
    opacity: 0,
    scale: 0.8,
    stagger: 0.2,
    ease: "back.inOut",
  })

})


</script>

<template>
  <div class="ceo-two-component">

    <div class="containerul_taburi">

      <div class="tab_elemet">
        <div class="tab_label label_default ">
          Flights
        </div>
        <div class="linie_tab"></div>
      </div>

      <div class="tab_elemet">
        <div class="tab_label">
          Hotels
        </div>
        <div class="linie_tab_default"></div>
      </div>

    </div>

    <div class="ceo_scroll_group">

      <div class="ceo_card_group_2 group_para">

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Paris
            </div>

            <div class="ceo_card_title_country">
              France
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Rome
            </div>

            <div class="ceo_card_title_country">
              Italy
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              New York City
            </div>

            <div class="ceo_card_title_country">
              USA
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

      </div>
      <div class="ceo_card_group_2 group_para">

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Tokyo
            </div>

            <div class="ceo_card_title_country">
              Japan
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              London
            </div>

            <div class="ceo_card_title_country">
              United Kingdom
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Barcelona
            </div>

            <div class="ceo_card_title_country">
              Spain
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

      </div>
      <div class="ceo_card_group_2 group_para">

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Dubai
            </div>

            <div class="ceo_card_title_country">
              United Arab Emirates
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Bangkok
            </div>

            <div class="ceo_card_title_country">
              Thailand
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Istanbul
            </div>

            <div class="ceo_card_title_country">
              Turkey
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

      </div>
      <div class="ceo_card_group_2 group_para">

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Singapore
            </div>

            <div class="ceo_card_title_country">
              Singapore
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Amsterdam
            </div>

            <div class="ceo_card_title_country">
              Netherlands
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Sydney
            </div>

            <div class="ceo_card_title_country">
              Australia
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

      </div>

      <div class="ceo_card_group_2">

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Prague
            </div>

            <div class="ceo_card_title_country">
              Czech Republic
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Vienna
            </div>

            <div class="ceo_card_title_country">
              Austria
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Cape Town
            </div>

            <div class="ceo_card_title_country">
              South Africa
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

      </div>
      <div class="ceo_card_group_2">

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Rio de Janeiro
            </div>

            <div class="ceo_card_title_country">
              Brazil
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Seoul
            </div>

            <div class="ceo_card_title_country">
              South Korea
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Lisbon
            </div>

            <div class="ceo_card_title_country">
              Portugal
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

      </div>
      <div class="ceo_card_group_2">

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Paris
            </div>

            <div class="ceo_card_title_country">
              France
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Hong Kong
            </div>

            <div class="ceo_card_title_country">
              China
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Mexico City
            </div>

            <div class="ceo_card_title_country">
              Mexico
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

      </div>
      <div class="ceo_card_group_2">

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Paris
            </div>

            <div class="ceo_card_title_country">
              France
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              Rome
            </div>

            <div class="ceo_card_title_country">
              Italy
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

        <div class="ceo_card_element_2">

          <div class="ceo_card_title_group_2">
            <div class="ceo_card_title_city">
              New York City
            </div>

            <div class="ceo_card_title_country">
              USA
            </div>

          </div>

          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path class="svg_color" d="M2 5L7.92929 10.9293C7.96834 10.9683 8.03166 10.9683 8.07071 10.9293L14 5"
              stroke="black" stroke-opacity="0.72" stroke-width="1.5" stroke-linecap="round" />
          </svg>

        </div>

      </div>

    </div>

  </div>

</template>

<style scoped>
.ceo-two-component {
  margin-top: 180px;
  display: flex;
  padding: 0px 132px;
  flex-direction: column;
  align-items: center;
  gap: 32px;
  align-self: stretch;
  ;
}

.ceo_scroll_group {
  display: flex;
  height: 288px;
  flex-direction: column;
  align-items: flex-start;
  gap: 32px;
  align-self: stretch;
  overflow-y: auto;
  padding: 16px;
}

/* modificare scroll */

.ceo_scroll_group::-webkit-scrollbar {
  width: 4px;
}


.ceo_scroll_group::-webkit-scrollbar-track {
  background: rgba(0, 0, 0, 0);
  border-radius: 8px;
}

.ceo_scroll_group::-webkit-scrollbar-thumb {
  background: rgba(0, 0, 0, 0.06);
  border-radius: 8px;
}


.ceo_scroll_group::-webkit-scrollbar-thumb:hover {
  background: rgba(0, 0, 0, 0.24);
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

/* carduri CEO */

.ceo_card_group_2 {
  display: flex;
  align-items: center;
  gap: 24px;
  align-self: stretch;
}

.ceo_card_element_2 {
  display: flex;
  padding: 12px 20px;
  justify-content: space-between;
  align-items: center;
  flex: 1 0 0;

  border-radius: 16px;
  background: #FFF;
  box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.08);


  cursor: pointer;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.ceo_card_element_2:hover {
  box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.12);
  transform: translateY(-4px);
}

.ceo_card_title_group_2 {
  display: flex;
  align-items: center;
  gap: 12px;
}

.ceo_card_title_city {
  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 24px;
  /* 150% */
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.ceo_card_element_2:hover .ceo_card_title_city {
  color: #816EFC;
}

.ceo_card_title_country {
  color: rgba(0, 0, 0, 0.72);
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  /* 150% */
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);

}

.ceo_card_element_2:hover .ceo_card_title_country {
  color: #816EFC;
}

.svg_color {
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.ceo_card_element_2:hover .svg_color {
  stroke: #816EFC;
  stroke-width: 2.4px;
}
</style>
