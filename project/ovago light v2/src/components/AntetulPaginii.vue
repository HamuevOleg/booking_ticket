<script setup>

import SearchIcon from './icons/IconSearch.vue'
import MeniulPrincipal from './MeniulPrincipal.vue'

// ====== Importare biblioteca paralax ======

import { gsap } from "gsap"
import { ScrollTrigger } from "gsap/ScrollTrigger"
import { MorphSVGPlugin } from "gsap/MorphSVGPlugin";

gsap.registerPlugin(MorphSVGPlugin);


import { ref, computed, onMounted, onBeforeUnmount } from 'vue'

const open = ref(false) // creez variabila pentru a controla prezenta modalului

const isLarge = ref(false)
const boxRef = ref(null)

// const boxStyle = computed(() => ({
//   flex: isLarge.value ? '2.28' : '',
//   background: isLarge.value ? 'rgba(33, 0, 93, 0.04)' : '',
//   padding: isLarge.value ? '24px 0px 24px 24px' : '',
// }))

// const lineStyle = computed(() => ({
//   opacity: isLarge.value ? '0' : '',
// }))

const expandBox = () => {
  isLarge.value = true
}

const handleClickOutside = (event) => {
  if (boxRef.value && !boxRef.value.contains(event.target)) {
    isLarge.value = false
    open.value = false
  }
}

onMounted(() => {
  document.addEventListener('click', handleClickOutside)
})

onBeforeUnmount(() => {
  document.removeEventListener('click', handleClickOutside)
})

gsap.registerPlugin(ScrollTrigger)


onMounted(() => {

  // ========= Aceasta este animatia avatar =========

  const animatieIcon = document.querySelector('.buton_menu');

  animatieIcon.addEventListener('mouseenter', () => {
    gsap.to("#circle", {
      duration: 0.6,
      morphSVG: "#hippo",
      ease: 'power2.inOut'
    })
  });

  animatieIcon.addEventListener('mouseleave', () => {
    gsap.to("#circle", {
      duration: 0.6,
      morphSVG: "#circle",
      ease: 'power2.inOut'
    })
  });


  // ========= Aceasta este animatia pentru miscare =========

  gsap.to(".containerul_taburi_header", {
    scrollTrigger: {
      trigger: ".hot_offer_component",
      start: "top 45%",
      end: "+=100",
      // markers: true,
      scrub: true,
    },
    opacity: 0,
    y: 16,
  })

  gsap.from(".mini_search_component", {
    scrollTrigger: {
      trigger: ".hot_offer_component",
      start: "top 26%",
      end: "+=100",
      // markers: true,
      scrub: true,
    },
    opacity: 0,
    y: 32,
    scale: 1.1,
  })


})

</script>

<template>
  <div class="antet_bloc_principal">

    <svg class="logo_anim" xmlns="http://www.w3.org/2000/svg" width="296" height="32" viewBox="0 0 256 32">
      <path class="litera_4"
        d="M88.1566 25.7651C86.4595 27.5016 84.0353 28.3922 81.0048 28.3922C74.3437 28.3922 69.772 22.7672 69.772 16.2816C69.772 11.5387 72.1498 6.89214 76.6005 5.01706C81.1729 3.09064 86.3843 4.43285 89.2071 8.57892L86.1766 11.0723C84.8579 9.37673 83.1983 8.35621 81.0451 8.35621C76.6905 8.35621 73.9743 12.0576 73.9743 16.2816C73.9743 20.5256 76.6236 24.3405 81.0451 24.3405C83.9564 24.3405 86.7018 22.7892 86.7018 19.5319H81.8533V15.6137H90.6615L90.6618 16.0641C90.6665 19.5268 90.6715 23.0597 88.1566 25.7651Z"
        fill="#5D50B4" />
      <path class="litera_2"
        d="M49.8734 3.6743H44.837L37.8778 18.3391L30.9186 3.6743H25.8822L37.8778 28.9554L49.8734 3.6743Z"
        fill="#5D50B4" />
      <path class="litera_1" fill-rule="evenodd" clip-rule="evenodd"
        d="M25.9279 16.2699C25.9279 23.2634 19.7769 28.5055 13.2001 28.5055C6.50728 28.5055 0.517578 23.1894 0.517578 16.2699C0.517578 9.26156 6.66856 4.03413 13.2458 4.03413C19.895 4.03413 25.9279 9.36669 25.9279 16.2699ZM13.2001 8.26263C17.5204 8.26263 21.1665 11.692 21.1665 16.1799C21.1665 20.5074 17.5057 24.1422 13.2458 24.1422C8.94521 24.1422 5.27931 20.6769 5.27931 16.2249C5.27931 11.8757 8.91101 8.26263 13.2001 8.26263Z"
        fill="#5D50B4" />
      <path class="litera_5" fill-rule="evenodd" clip-rule="evenodd"
        d="M105.755 28.5991C112.332 28.5991 118.483 23.357 118.483 16.3635C118.483 9.46027 112.45 4.12771 105.801 4.12771C99.2234 4.12771 93.0725 9.35515 93.0725 16.3635C93.0725 23.2829 99.0622 28.5991 105.755 28.5991ZM113.721 16.2735C113.721 11.7856 110.075 8.35621 105.755 8.35621C101.466 8.35621 97.8342 11.9692 97.8342 16.3185C97.8342 20.7704 101.5 24.2357 105.801 24.2357C110.061 24.2357 113.721 20.6011 113.721 16.2735Z"
        fill="#5D50B4" />
      <path class="litera_3" fill-rule="evenodd" clip-rule="evenodd"
        d="M61.4729 22.1179L64.0826 27.9208H68.9815L57.3275 3.04449L45.4482 27.9208H50.3471L53.0025 22.1179H61.4729ZM57.2606 12.5362L54.7881 18.2492H59.7788L57.2606 12.5362Z"
        fill="#5D50B4" />
    </svg>


    <div class="containerul_taburi_header">
      <div class="tab_elemet">
        <div class="tab_label">
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



    <div class="mini_search_component">
      <div class="mini_group">
        <div class="mini_text">
          New York - Istanbul
        </div>
        <div class="mini_divider"></div>
        <div class="mini_text">
          20 Oct - 27 Oct
        </div>
        <div class="mini_divider"></div>
        <div class="mini_text">
          1 Adult
        </div>
      </div>

      <div class="mini_buttom">
        <SearchIcon />
      </div>
    </div>


    <div class="telefon_menu">

      <div class="suport_button">
        USD
      </div>

      <div class="suport_button">
        Support 24/7
      </div>

      <div ref="boxRef" @click="expandBox" class="buton_menu">

        <div class="menu_icon_container">

          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
            <path
              d="M12 15.25C13.0424 15.25 15.1503 15.3914 17.0264 16.1357C18.9112 16.8837 20.75 18.3351 20.75 21C20.75 21.4142 20.4142 21.75 20 21.75C19.5858 21.75 19.25 21.4142 19.25 21C19.25 19.2205 18.0887 18.1712 16.4736 17.5303C14.8498 16.8859 12.9575 16.75 12 16.75C11.0425 16.75 9.15016 16.8859 7.52637 17.5303C5.91133 18.1712 4.75 19.2205 4.75 21C4.75 21.4142 4.41421 21.75 4 21.75C3.58579 21.75 3.25 21.4142 3.25 21C3.25 18.3351 5.08876 16.8837 6.97363 16.1357C8.84974 15.3914 10.9576 15.25 12 15.25Z"
              fill="#816EFC" />

            <path id="hippo" fill-rule="evenodd" clip-rule="evenodd"
              d="M11.4772 0.0764996C15.7938 -0.468524 17.2997 2.02058 17.5134 3.33334L17.9343 6.47494C17.7452 6.56947 17.4214 6.70777 16.988 6.86556C17.1565 7.38016 17.2497 7.92941 17.2497 8.50033C17.2495 11.3997 14.8991 13.7503 11.9997 13.7503C9.10038 13.7502 6.74987 11.3996 6.74968 8.50033C6.74968 8.47501 6.7503 8.44939 6.75066 8.42416C4.09964 8.57726 1.74714 8.59326 1.62175 8.27767C1.37488 7.64929 4.75068 7.14493 5.77214 6.94759V3.89193C5.77218 2.42034 6.0815 0.757782 11.4772 0.0764996ZM15.5583 7.31673C14.9871 7.4734 14.3388 7.62721 13.6315 7.7513C12.5439 7.94209 10.4183 8.16561 8.25359 8.32455C8.25091 8.38269 8.24968 8.44153 8.24968 8.50033C8.24987 10.5712 9.92881 12.2502 11.9997 12.2503C14.0706 12.2503 15.7495 10.5712 15.7497 8.50033C15.7497 8.08675 15.6819 7.68879 15.5583 7.31673Z"
              fill="#816EFC" />

            <path id="circle" fill-rule="evenodd" clip-rule="evenodd"
              d="M12 2.25C14.8995 2.25 17.25 4.60051 17.25 7.5C17.25 10.3995 14.8995 12.75 12 12.75C9.1005 12.75 6.75 10.3995 6.75 7.5C6.75 4.60051 9.1005 2.25 12 2.25ZM12 3.75C9.92893 3.75 8.25 5.42893 8.25 7.5C8.25 9.57107 9.92893 11.25 12 11.25C14.0711 11.25 15.75 9.57107 15.75 7.5C15.75 5.42893 14.0711 3.75 12 3.75Z"
              fill="#816EFC" />
          </svg>

        </div>

        <div class="container_menu">

          <div class="elemet_linie_menu_1"></div>
          <div class="elemet_linie_menu_2"></div>
          <div class="elemet_linie_menu_1"></div>

        </div>

        <Transition>
          <MeniulPrincipal v-show="isLarge" class="menu_modal_position" />
        </Transition>


      </div>

    </div>

  </div>

</template>


<style scoped>
#hippo {
  visibility: hidden;
}

.v-enter-active,
.v-leave-active {
  opacity: 1;
  transform: translateX(0px);
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
  transform: translateX(48px);
}

.menu_modal_position {
  position: absolute;
  top: 44px;
  right: 0px;
  z-index: 99;
  /* transition: all 400ms cubic-bezier(0.3, 0, 0, 1); */
}

.mini_search_component {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: inline-flex;
  padding: 8px 8px 8px 24px;
  justify-content: flex-end;
  align-items: center;
  gap: 24px;

  border-radius: 40px;
  border: 1px solid rgba(0, 0, 0, 0.08);
  background: rgba(255, 255, 255, 0.68);
  backdrop-filter: blur(16px);

  /* opacity: 0; */


}

.mini_text {
  overflow: hidden;
  color: #000;
  text-overflow: ellipsis;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  /* 150% */
  letter-spacing: 0.64px;
}

.mini_buttom {
  display: flex;
  padding: 10px;
  align-items: center;
  gap: 12px;

  border-radius: 40px;
  background: #816EFC;
}

.mini_divider {
  width: 1px;
  height: 24px;

  stroke-width: 1px;
  background-color: rgba(0, 0, 0, 0.16);
}

.mini_group {
  display: flex;
  align-items: center;
  gap: 16px;
}

/* .antet_logo{
    padding-right: 138px;
  } */

.logo_anim {
  cursor: pointer;
  transition: all 300ms cubic-bezier(0.3, 0, 0, 1);
}

.litera_1 {
  transition: all 300ms cubic-bezier(0.3, 0, 0, 1);
}

.litera_2 {
  transition: all 300ms cubic-bezier(0.3, 0, 0, 1);
}

.litera_3 {
  transition: all 300ms cubic-bezier(0.3, 0, 0, 1);
}

.litera_4 {
  transition: all 300ms cubic-bezier(0.3, 0, 0, 1);
}

.litera_5 {
  transition: all 300ms cubic-bezier(0.3, 0, 0, 1);
}

.logo_anim:hover .litera_1 {
  fill: #816EFC;
  transform: translateX(2px);
}

.logo_anim:hover .litera_2 {
  fill: #816EFC;
  transform: translateX(4px);
}

.logo_anim:hover .litera_3 {
  fill: #816EFC;
  transform: translateX(6px);
}

.logo_anim:hover .litera_4 {
  fill: #816EFC;
  transform: translateX(8px);
}

.logo_anim:hover .litera_5 {
  fill: #816EFC;
  transform: translateX(10px);
}

.header {
  position: sticky;
  top: 0;

  padding: 10px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
  /* Optional shadow effect */
  z-index: 1000;
  /* Ensures it stays above other elements */
}

.antet_bloc_principal {

  display: flex;
  padding: 24px 132px 24px 132px;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;

  position: sticky;
  top: 0;

  z-index: 100;

  border-radius: 24px;
  border: 1px solid rgba(255, 255, 255, 0.24);
  background: rgba(255, 255, 255, 0.48);
  backdrop-filter: blur(16px);


}

/* .numarul_telefon{
    color: #000;
    text-align: center;
    font-family: Jost;
    font-size: 24px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
  } */

.suport_button {

  display: flex;
  padding: 4px 16px;
  justify-content: center;
  align-items: center;

  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 24px;

  border-radius: 60px;
  background: rgba(33, 0, 93, 0);

  cursor: pointer;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);

}

.suport_button:hover {
  background: rgba(33, 0, 93, 0.04);
  padding: 8px 16px;

}

/* taburile */

.containerul_taburi_header {
  display: flex;
  height: 46px;
  justify-content: center;
  align-items: center;
  gap: 56px;
  flex-shrink: 0;
}

.tab_elemet {

  display: flex;
  padding: 12px 0px;
  justify-content: center;
  align-items: center;

  position: relative;

  cursor: pointer;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  z-index: 2;
}

.tab_label {
  color: #000;
  text-overflow: ellipsis;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  letter-spacing: 0.72px;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.tab_elemet:hover .tab_label {
  transform: translateY(-4px);
}


.linie_tab {
  position: absolute;
  top: 96%;
  width: 6px;
  height: 2px;
  background-color: #000;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.tab_elemet:hover .linie_tab {

  transform: scaleX(1.5);

}

.linie_tab_default {
  position: absolute;
  top: 96%;
  width: 6px;
  height: 2px;
  background-color: #000;

  transform: scaleX(1);
  opacity: 0;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.tab_elemet:hover .linie_tab_default {

  transform: scaleX(1.5);
  opacity: 0.16;

}

.telefon_menu {
  display: inline-flex;
  align-items: center;
  gap: 12px;
}

/* butonul menu */

.buton_menu {
  display: flex;
  padding: 4px 10px 4px 4px;
  justify-content: center;
  align-items: center;
  gap: 8px;

  border-radius: 24px;
  background: #816EFC;

  cursor: pointer;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  position: relative;
}

.buton_menu:hover {
  background: rgba(129, 110, 252, 0.80);
}

.menu_icon_container {
  display: flex;
  padding: 4px;
  align-items: center;
  gap: 10px;

  border-radius: 16px;
  background: #FFF;
}

.container_menu {
  display: flex;
  width: 18px;
  height: 24px;
  padding: 0px 3px;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 4px;
}



.elemet_linie_menu_1 {
  height: 2px;
  flex-shrink: 0;
  align-self: stretch;

  border-radius: 2px;
  background: #FFF;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.elemet_linie_menu_2 {
  width: 14px;
  height: 2px;
  flex-shrink: 0;

  border-radius: 2px;
  background: #FFF;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}


.buton_menu:hover .elemet_linie_menu_2 {
  transform: scaleX(1.4)
}

.buton_menu:hover .elemet_linie_menu_1 {
  transform: scaleX(0.6)
}
</style>
