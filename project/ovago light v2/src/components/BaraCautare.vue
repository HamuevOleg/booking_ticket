<script setup>
import FromIcon from './icons/IconFrom.vue'
import WhereIcon from './icons/IconWhere.vue'
import CalendarIcon from './icons/IconCalendar.vue'
import UserIcon from './icons/IconUser.vue'
import SearchIcon from './icons/IconSearch.vue'
import WidgetModal from './WidgetModal.vue'


import { gsap } from "gsap"
import { ScrollTrigger } from "gsap/ScrollTrigger"



import { ref, computed, onMounted, onBeforeUnmount } from 'vue'

const open = ref(false) // creez variabila pentru a controla prezenta modalului

const isLarge = ref(false)
const boxRef = ref(null)

const boxStyle = computed(() => ({
  flex: isLarge.value ? '2.28' : '',
  background: isLarge.value ? 'rgba(33, 0, 93, 0.04)' : '',
  padding: isLarge.value ? '24px 0px 24px 24px' : '',
}))

const lineStyle = computed(() => ({
  opacity: isLarge.value ? '0' : '',
}))

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

const paddingMeuRight = ref(22)
const marginSearch = ref(312)



gsap.registerPlugin(ScrollTrigger)

onMounted(() => {

  // ========= aici este animatia =========

  gsap.to(".icon_parallax", {
    scrollTrigger: {
      trigger: ".hot_offer_component",
      start: "top 30%",
      end: "+=380",
      // markers: true,
      scrub: true,
      // toggleActions: "restart pause reverse pause"
      // pin: true,
      onUpdate: function (self) {
        paddingMeuRight.value = 24 - self.progress * 16;
        marginSearch.value = 312 + self.progress * 460;
        // console.log(paddingMeuRight.value)
      }
    },
    ease: 'none',
    // scale:0,
    opacity: 0,

  })


  gsap.to(".search_field", {
    scrollTrigger: {
      trigger: ".hot_offer_component",
      start: "top 30%",
      end: "+=380",
      // markers: true,
      scrub: true,
      // toggleActions: "restart pause reverse pause"
      // pin: true,
    },
    y: -100,
    ease: 'none',
    opacity: -3,
    // scale:0.6,
    scale: 0.7,
    duration: 1,
  })

})


</script>

<template>
  <div class="search_field"
    :style="{ 'margin-left': marginSearch + 'px', 'margin-right': marginSearch + 'px', 'margin-top': '0px', 'margin-bottom': '0px' }">
    <div class="search_group">

      <div ref="boxRef" :style="boxStyle" @click="expandBox" class="search_in">
        <div class="icon_value">
          <FromIcon class="icon_imput icon_parallax" /> New York
        </div>
        <div :style="lineStyle" class="line_divid"></div>

        <Transition>
          <WidgetModal v-show="isLarge" class="widget_modal_position " />
        </Transition>

      </div>

      <div @click="open = false" class="search_in" :style="{ 'padding-left': paddingMeuRight + 'px' }">
        <div class="icon_value">
          <WhereIcon class="icon_parallax" /> Istanbul
        </div>
        <div class="line_divid"></div>
      </div>

      <div class="search_in" :style="{ 'padding-left': paddingMeuRight + 'px' }">
        <div class="icon_value">
          <CalendarIcon class="icon_parallax" /> 20 Oct - 27 Oct
        </div>
        <div class="line_divid"></div>
      </div>

      <div class="search_in" :style="{ 'padding-left': paddingMeuRight + 'px' }">
        <div class="icon_value">
          <UserIcon class="icon_parallax" /> 1 Adult, Business
          <div class="line_divid" :style="{ opacity: 0 }"></div>
        </div>
      </div>

    </div>
    <div class="button_search">
      <SearchIcon class="icon_search" /> Search
    </div>
  </div>

</template>

<style scoped>
.v-enter-active,
.v-leave-active {
  opacity: 1;
  transform: translateX(0px);
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
  transform: translateX(-48px);
}

.widget_modal_position {
  position: fixed;
  bottom: -470px;
  left: -2px;
  z-index: 99;
  /* transition: all 400ms cubic-bezier(0.3, 0, 0, 1); */
}

.icon_value {
  display: flex;
  align-items: center;
  gap: 12px;
}

.line_divid {
  width: 1px;
  height: 32px;
  background-color: rgba(0, 0, 0, 0.12);
  transition: all 200ms cubic-bezier(0.3, 0, 0, 1);
}

.search_in:hover .line_divid {
  background-color: rgba(255, 255, 255, 0);
}

.search_field {
  display: flex;
  justify-content: center;
  align-items: center;
  align-self: stretch;

  margin: 0px 312px 0px 312px;

  padding: 8px;
  gap: 16px;

  border-radius: 52px;
  border: 1px solid rgba(33, 0, 93, 0.08);
  background: #FFF;
  box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.12);
  position: relative;
  z-index: 5;
}

.search_group {
  display: flex;
  align-items: center;
  gap: 8px;
  height: 64px;
  flex-grow: 1;
  /* padding-right: 8px;
    padding-left: 4px; */
}

.search_in {
  display: flex;
  padding: 12px 0px 12px 24px;
  flex: 1;
  justify-content: space-between;
  align-items: center;
  border-radius: 56px;
  color: rgb(0, 0, 0);
  text-overflow: ellipsis;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 16px;
  /* 114.286% */
  letter-spacing: 0.56px;
  /* border: 1px solid rgba(255, 255, 255, 0); */
  background-color: rgba(0, 0, 0, 0);

  cursor: pointer;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  position: relative;
}

.search_in:hover {
  padding: 22px 0px 22px 24px;
  /* border: 1px solid rgba(0, 0, 0, 0.24); */
  background: rgba(33, 0, 93, 0.04);
}

/* .search_in:active{
      padding: 22px 0px 22px 24px;

      background: rgba(33, 0, 93, 0.04);
      flex: 2.16;
    } */

.icon_value ::v-deep(svg) {
  fill: #000000;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.search_in:active .icon_value ::v-deep(svg) {
  fill: #000;
}


.search_in:active {
  padding: 20px 0px 20px 24px;
  /* border: 1px solid rgba(255, 255, 255, 0.24); */
  background-color: rgba(24, 0, 100, 0.06);
  color: black;
}

.button_search {
  display: inline-flex;
  padding: 24px;
  justify-content: center;
  align-items: center;
  gap: 12px;

  border-radius: 56px;
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
  position: relative;

  z-index: 2;
}

.button_search:hover {
  background: rgba(129, 110, 252, 0.90);
  padding: 24px 24px 24px 60px;

}

.button_search:active {
  background: rgba(129, 110, 252, 1);

}

.button_search .icon_search {
  position: absolute;
  left: 30px;
  top: 48%;
  transform: translateY(-50%);
  opacity: 0;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  cursor: pointer;

}

.button_search:hover .icon_search {
  left: 24px;
  opacity: 1;
  cursor: pointer;
}
</style>