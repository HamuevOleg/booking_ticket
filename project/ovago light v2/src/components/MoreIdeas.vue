<script setup>

  import SteaLocatie from "./LocatieStea.vue"

  import { ref } from 'vue'

  import oraParis from '/src/components/media/map_image_paris.png'
  import oraLondon from '/src/components/media/map_image_londra.png'
  import oraBarcelona from '/src/components/media/map_image_barcelona.png'
  import oraRoma from '/src/components/media/map_image_roma.png'
  import oraBerlin from '/src/components/media/map_image_berlin.png'
  import oraSantorini from '/src/components/media/map_image_santo.png'
  import oraChisinau from '/src/components/media/map_image_chisinau.png'

  import oraCarParis from '/src/components/media/paris_card.png'
  import oraCarLondon from '/src/components/media/london_card.png'
  import oraCarBarcelona from '/src/components/media/barcelona_card.png'
  import oraCarRoma from '/src/components/media/roma_card.png'
  import oraCarBerlin from '/src/components/media/berlin_card.png'
  import oraCarSantorini from '/src/components/media/santo_card.png'
  import oraCarChisinau from '/src/components/media/chisinau_card.png'

  const isHoveredParis = ref(false)
  const isHoveredLondon = ref(false)
  const isHoveredBarcelona = ref(false)
  const isHoveredRoma = ref(false)
  const isHoveredBerlin = ref(false)
  const isHoveredSantorini = ref(false)
  const isHoveredChisinau = ref(false)

  import CardMap from "./CardMap.vue"


  // ====== Importare biblioteca paralax ======

  import { gsap } from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  import { onMounted } from "vue"
  isHoveredChisinau

  gsap.registerPlugin(ScrollTrigger)


  onMounted(() => {

    gsap.set(".stea_decor", {
      rotation:-360,
      y:-600,
      x:-600,
      scale:0.2,
      opacity:0.2
    })

    gsap.to(".stea_decor", {
      scrollTrigger:{
        trigger: ".inspiratie_component_map",
        start: "top bottom",
        end: "bottom bottom",
        // markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
      },
      rotation:0,
      y:0,
      x:0,
      scale:1,
      opacity:1,
    })

    gsap.set(".savor", {
      rotation:-120,
      opacity:-0.5,
    })

    gsap.to(".savor", {
      scrollTrigger:{
        trigger: ".inspiratie_component_map",
        start: "top bottom",
        end: "center center",
        // markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
      },
      rotation:-15,
      ease: 'none',
      opacity:1,
    })

    gsap.set(".pin_paralax", {
      y:88,
      scale:0.3,
      opacity:0.5
    })

    gsap.to(".pin_paralax", {
      scrollTrigger:{
        trigger: ".harta_pinuri",
        start: "top center",
        end: "90% bottom",
        // markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
        
      },
      y:0,
      ease: 'none',
      stagger: 0.3,
      scale:1,
      opacity:1,
    })

    gsap.from(".map_parallax", {
      scrollTrigger: {
        trigger: ".inspiratie_component_map",
        start: "top 80%",
        end: "top center",
      // markers: true,
      scrub: true
    },
      y:-180,
      ease:"power2inOut",
      opacity:0,
      scale:0.6,
      stagger:{
        each: 0.2,
        from: 'end',
      },
      fontWeight:200,
      // rotation:30,
    })


  })


</script>

<template>

  <div class="inspiratie_component_map">

    <div class="titlu_taburi">
      <div class="titlu_inspiration map_parallax">
        Need more ideas for your next trip?
      </div>

      <div class="containerul_taburi map_parallax">

        <div class="tab_elemet">
          <div class="tab_label">
            Africa          
          </div> 
          <div class="linie_tab_default"></div>
        </div>

        <div class="tab_elemet">
          <div class="tab_label">
            Latin America          
          </div> 
          <div class="linie_tab_default"></div>
        </div>

        <div class="tab_elemet">
          <div class="tab_label label_default">
            Europe          
          </div> 
          <div class="linie_tab"></div>
        </div>

        <div class="tab_elemet">
          <div class="tab_label">
            Middle East          
          </div> 
          <div class="linie_tab_default"></div>
        </div>

        <div class="tab_elemet">
          <div class="tab_label">
            Asia & Oceania          
          </div> 
          <div class="linie_tab_default"></div>
        </div>

      </div>

    </div>

    <div class="harta_pinuri">

      <svg class="stea_decor" xmlns="http://www.w3.org/2000/svg" width="86" height="86" viewBox="0 0 86 86" fill="none">
        <path d="M53.2899 6.14986C48.6291 -1.61821 37.3709 -1.61821 32.7101 6.14986L24.2935 20.1775C23.2801 21.8665 21.8665 23.2801 20.1775 24.2935L6.14986 32.7101C-1.61821 37.3709 -1.61821 48.6291 6.14986 53.2899L20.1775 61.7065C21.8665 62.7199 23.2801 64.1335 24.2935 65.8225L32.7101 79.8501C37.3709 87.6182 48.6291 87.6182 53.2899 79.8501L61.7065 65.8225C62.7199 64.1335 64.1335 62.7199 65.8225 61.7065L79.8501 53.2899C87.6182 48.6291 87.6182 37.3709 79.8501 32.7101L65.8225 24.2935C64.1335 23.2801 62.7199 21.8665 61.7065 20.1775L53.2899 6.14986Z" fill="url(#paint0_linear_318_7339)" fill-opacity="0.7"/>
        <defs>
          <linearGradient id="paint0_linear_318_7339" x1="72.3526" y1="13.4803" x2="13.4803" y2="72.3526" gradientUnits="userSpaceOnUse">
            <stop stop-color="#AB9FFF"/>
            <stop offset="1" stop-color="#FFDEF3"/>
          </linearGradient>
        </defs>
      </svg>

      <div class="savor">
        🍹 Savor the <br>moment!
      </div>

      <div class="pozitionare_london_pin pin_paralax">
        <SteaLocatie 
          @mouseover="isHoveredLondon = true"
          @mouseleave="isHoveredLondon = false"
          :imageSrc="oraLondon" 
        /> 
      </div>

      <Transition name="slide">
        <CardMap
          v-show="isHoveredLondon"
          class="pozitionare_london_card "
          :imagSrc="oraCarLondon" 
          titleSrc='London, England' priceSrc='$650*'
        />
      </Transition> 

      <div class="pozitionare_berlin_pin pin_paralax">
        <SteaLocatie 
          @mouseover="isHoveredBerlin = true"
          @mouseleave="isHoveredBerlin = false"
          :imageSrc="oraBerlin" 
        /> 
      </div>
      
      <Transition name="slide">
        <CardMap
          v-show="isHoveredBerlin"
          class="pozitionare_berlin_card"
          :imagSrc="oraCarBerlin" 
          titleSrc='Berlin, Germany' priceSrc='$290*'
        />
      </Transition> 


      <div class=" pozitionare_paris_pin pin_paralax">
        <SteaLocatie 
          @mouseover="isHoveredParis = true"
          @mouseleave="isHoveredParis = false"
          :imageSrc="oraParis" 
        /> 
      </div>

      <Transition name="slide">
        <CardMap
          v-show="isHoveredParis"
          class="pozitionare_paris_card "
          :imagSrc="oraCarParis" 
          titleSrc='Paris, France' priceSrc='$450*'
        />
      </Transition> 

      <div class="pozitionare_chisinau_pin pin_paralax">
        <SteaLocatie 
          @mouseover="isHoveredChisinau = true"
          @mouseleave="isHoveredChisinau = false"
          :imageSrc="oraChisinau" 
        /> 
      </div>

      <Transition name="slide">
        <CardMap
          v-show="isHoveredChisinau"
          class="pozitionare_chisinau_card"
          :imagSrc="oraCarChisinau" 
          titleSrc='Chisinau, Moldova' priceSrc='$295*'
        />
      </Transition>  

      <div class="pozitionare_barcelona_pin pin_paralax">
        <SteaLocatie 
          @mouseover="isHoveredBarcelona = true"
          @mouseleave="isHoveredBarcelona = false"
          :imageSrc="oraBarcelona"  
        /> 
      </div>

      <Transition name="slide">
        <CardMap
          v-show="isHoveredBarcelona"
          class="pozitionare_barcelona_card"
          :imagSrc="oraCarBarcelona" 
          titleSrc='Barcelona, Spain' priceSrc='$328*'
        />
      </Transition>   

      <div class="pozitionare_roma_pin pin_paralax">
        <SteaLocatie 
          @mouseover="isHoveredRoma = true"
          @mouseleave="isHoveredRoma = false"
          :imageSrc="oraRoma" 
        /> 
      </div>

      <Transition name="slide">
        <CardMap
          v-show="isHoveredRoma"
          class="pozitionare_roma_card"
          :imagSrc="oraCarRoma" 
          titleSrc='Rome, Italy' priceSrc='$422*'
        />
      </Transition> 
      
      <div class="pozitionare_santorini_pin pin_paralax">
        <SteaLocatie 
          @mouseover="isHoveredSantorini = true"
          @mouseleave="isHoveredSantorini = false"
          :imageSrc="oraSantorini" 
        /> 
      </div>

      <Transition name="slide">
        <CardMap
          v-show="isHoveredSantorini"
          class="pozitionare_santorini_card"
          :imagSrc="oraCarSantorini" 
          titleSrc='Santorini, Greece' priceSrc='$295*'
        />
      </Transition>
      




      <img src="/src/components/media/map.svg" alt="" srcset="">

    </div>

   

  </div>







 
</template>

<style scoped>

  .harta_pinuri{
    position: relative;
  }
  .pozitionare_paris_pin{
    position: absolute;
    top: 515px;
    left: 420px;
    z-index: 2;
  }  
    .pozitionare_paris_card{
      position: absolute;
      top: 208px;
      left: 533px;
      z-index: 3;
      opacity: 1;
    }

  .pozitionare_london_pin{
    position: absolute;
    top: 348px;
    left: 308px;
    z-index: 1;
  }
    .pozitionare_london_card{
      position: absolute;
      top: 8px;
      left: 428px;
      z-index: 3;
      opacity: 1;
    }

  .pozitionare_barcelona_pin{
    position: absolute;
    top: 858px;
    left: 318px;
    z-index: 1;
  }
  .pozitionare_barcelona_card{
    position: absolute;
    top: 520px;
    left: 436px;
    z-index: 4;
    opacity: 1;
  }

  .pozitionare_roma_pin{
    position: absolute;
    top: 800px;
    left: 688px;
    z-index: 1;
  }
  .pozitionare_roma_card{
    position: absolute;
    top: 456px;
    left: 804px;
    z-index: 4;
    opacity: 1;
  }

  .pozitionare_berlin_pin{
    position: absolute;
    top: 318px;
    left: 720px;
    z-index: 1;
  }
  .pozitionare_berlin_card{
    position: absolute;
    top: 0px;
    left: 836px;
    z-index: 4;
    opacity: 1;
  }

  .pozitionare_santorini_pin{
    position: absolute;
    top: 1064px;
    left: 1128px;
    z-index: 1;
  }
  .pozitionare_santorini_card{
    position: absolute;
    top: 720px;
    left: 1248px;
    z-index: 4;
    opacity: 1;
  }

  .pozitionare_chisinau_pin{
    position: absolute;
    top: 594px;
    left: 1238px;
    z-index: 1;
  }
  .pozitionare_chisinau_card{
    position: absolute;
    top: 264px;
    left: 1360px;
    z-index: 4;
    opacity: 1;
  }


  .slide-enter-active, .slide-leave-active {
    transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
  }
  .slide-enter-from {
    opacity: 0;
    transform: translateY(-24px);
  }
  .slide-leave-to {
    opacity: 0;
    transform: translateY(24px);
  }

  .inspiratie_component_map{
    margin-top: 280px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 84px;

  }

  .titlu_taburi{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 64px;
  }



.titlu_inspiration{
  color: #000;
  font-family: Jost;
  font-size: 48px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

  /* taburile */

  .containerul_taburi{
    display: flex;
    height: 44px;
    justify-content: center;
    align-items: flex-end;
    gap: 32px;
  }

  .tab_elemet{

    display: flex;
    padding: 12px 0px;
    justify-content: center;
    align-items: center;

    position: relative;

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }
  
  .tab_label{
    color: rgba(0, 0, 0, 0.56);
    text-overflow: ellipsis;
    font-family: Jost;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 16px; /* 100% */
    letter-spacing: 0.64px;

    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .tab_elemet:hover .tab_label{
    transform: translateY(-4px);
  }


  .linie_tab{
    position: absolute;
    top: 96%;
    width: 100%;
    height: 1px;
    background-color: #000;

    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }
  
  .tab_elemet:hover .linie_tab{

    transform: scaleX(0.5);

  }

  .label_default{
    color: rgba(0, 0, 0, 1);
  }

  .linie_tab_default{
    position: absolute;
    top: 96%;
    width: 100%;
    height: 1px;
    background-color: #000;

    transform: scaleX(1);
    opacity: 0;

    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .tab_elemet:hover .linie_tab_default{

    transform: scaleX(0.5);
    opacity: 0.16;

  } 

  .stea_decor{
    position: absolute;
    top: 0;
    right: 0;

  }

  .savor{

    position: absolute;
    top: 280px;
    right: 74px;

    transform: rotate(-15deg);

    display: inline-flex;
    padding: 24px 72px;
    justify-content: center;
    align-items: center;

    border-radius: 24px;
    border: 1px solid rgba(202, 202, 202, 0.24);
    background: rgba(143, 130, 226, 0.08);
    backdrop-filter: blur(6px);

    color: #000;
    text-align: right;
    font-family: "Nothing You Could Do";
    font-size: 38px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
  }


</style>