<script setup>

// ====== Importare biblioteca paralax ======

import { gsap } from "gsap"
import { ScrollTrigger } from "gsap/ScrollTrigger"
import { onMounted } from "vue"

gsap.registerPlugin(ScrollTrigger)


onMounted(() => {

  gsap.from(".blog_main_title", {
    scrollTrigger: {
      trigger: ".blog_componet",
      start: "top bottom",
      end: "center 40%",
      //  markers: true,
      scrub: true,
      // toggleActions: "restart pause reverse pause"
    },
    y: -240,
    opacity: 0,
    scale: 0.4,
    stagger: 0.1,
    fontWeight: 100,
    ease: 'power1.inOut'
  })

  gsap.from(".blog_card", {
    scrollTrigger: {
      trigger: ".blog_componet",
      start: "10% bottom",
      end: "center 55%",
      //  markers: true,
      scrub: true,
      // toggleActions: "restart pause reverse pause"
    },
    y: 300,
    opacity: 0,
    stagger: 0.1,

    ease: 'power1.inOut'
  })

})

</script>

<template>
  <div class="blog_componet">

    <div class="blog_main_title">
      Travel Guides & Tips
    </div>

    <div class="blog_card_list">

      <div class="blog_card">

        <div class="blog_card_imag_bloc">
          <div class="blog_card_imag_bloc_imag">
          </div>
        </div>

        <div class="blog_card_info">
          <div class="blog_card_info_title">
            Best SPA Hotels in Spain: Barcelona, Málaga, <br>and Valencia Regions
          </div>

          <div class="blog_card_info_text">
            Choosing between nonstop and layover flights depends on your priorities—whether you're focused on saving
            time, cutting costs, or enjoying a layover adventure. Understanding the pros and cons of each can help you
            make the best decision for your next journey. Let AranGrant guide you in finding the perfect flight with our
            expert tips and
          </div>


        </div>

        <div class="tag_container">

          <div class="tag_componet">
            Business & First
          </div>

          <div class="tag_componet">
            Travel Strategies
          </div>

        </div>

      </div>

      <div class="blog_card">

        <div class="blog_card_imag_bloc">
          <div class="blog_card_imag_bloc_imag_2">
          </div>
        </div>

        <div class="blog_card_info">
          <div class="blog_card_info_title">
            Romantic Destinations for Couples: Your Best <br>Valentine’s Day Yet
          </div>

          <div class="blog_card_info_text">
            Choosing between nonstop and layover flights depends on your priorities—whether you're focused on saving
            time, cutting costs, or enjoying a layover adventure. Understanding the pros and cons of each can help you
            make the best decision for your next journey. Let AranGrant guide you in finding the perfect flight with our
            expert tips and
          </div>

        </div>

        <div class="tag_container">

          <div class="tag_componet">
            Business & First
          </div>

          <div class="tag_componet">
            Travel Strategies
          </div>

        </div>

      </div>

      <div class="blog_card">

        <div class="blog_card_imag_bloc">
          <div class="blog_card_imag_bloc_imag_3">
          </div>
        </div>

        <div class="blog_card_info">
          <div class="blog_card_info_title">
            Best SPA Hotels in Spain: Barcelona, Málaga, <br> and Valencia Regions
          </div>

          <div class="blog_card_info_text">
            Choosing between nonstop and layover flights depends on your priorities—whether you're focused on saving
            time, cutting costs, or enjoying a layover adventure. Understanding the pros and cons of each can help you
            make the best decision for your next journey. Let AranGrant guide you in finding the perfect flight with our
            expert tips and
          </div>




        </div>

        <div class="tag_container">

          <div class="tag_componet">
            Business & First
          </div>

          <div class="tag_componet">
            Travel Strategies
          </div>

        </div>

      </div>


    </div>


  </div>


</template>

<style scoped>
.blog_componet {
  margin-top: 240px;
  display: flex;
  padding: 0px 132px;
  flex-direction: column;
  align-items: center;
  gap: 56px;
  align-self: stretch;
}

.blog_main_title {
  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 32px;
  font-style: normal;
  font-weight: 500;
  line-height: 40px;
  /* 125% */
}

.blog_card_list {
  display: flex;
  justify-content: center;
  align-items: center;
  align-self: stretch;
  gap: 32px;
}

.blog_card {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 24px;

  cursor: pointer;
  /* transition: all 400ms cubic-bezier(0.3, 0, 0, 1); */
}

.blog_card_imag_bloc {
  display: flex;
  width: 524px;
  height: 380px;
  justify-content: center;
  align-items: center;
}

.blog_card_imag_bloc_imag {

  height: 380px;
  flex: 1 0 0;

  overflow: hidden;
  position: relative;

  border-radius: 40px;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);

}

.blog_card_imag_bloc_imag::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: inherit;

  background: url(/src/components/media/blog_1.jpg) lightgray center / 100% 100% no-repeat;

  background-size: 100%;
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
}

.blog_card:hover .blog_card_imag_bloc_imag::before {
  background-size: 108%;
  opacity: 0.8;
}

/* imaginea doi */

.blog_card_imag_bloc_imag_2 {

  height: 380px;
  flex: 1 0 0;

  overflow: hidden;
  position: relative;

  border-radius: 40px;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);

}

.blog_card_imag_bloc_imag_2::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: inherit;

  background: url(/src/components/media/blog_2.jpg) lightgray center / 100% 100% no-repeat;

  background-size: 100%;
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
}

.blog_card:hover .blog_card_imag_bloc_imag_2::before {
  background-size: 108%;
  opacity: 0.8;
}

/* imaginea trei */

.blog_card_imag_bloc_imag_3 {

  height: 380px;
  flex: 1 0 0;

  overflow: hidden;
  position: relative;

  border-radius: 40px;

  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);

}

.blog_card_imag_bloc_imag_3::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: inherit;

  background: url(/src/components/media/blog_3.jpg) lightgray center / 100% 100% no-repeat;

  background-size: 100%;
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
}

.blog_card:hover .blog_card_imag_bloc_imag_3::before {
  background-size: 108%;
  opacity: 0.8;
}

.blog_card_info {
  display: flex;
  padding: 0px 24px;
  flex-direction: column;
  align-items: flex-start;
  gap: 24px;
  align-self: stretch;

  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
}

.blog_card:hover .blog_card_info {
  opacity: 0.6;
}

.blog_card_info_title {
  align-self: stretch;

  color: #000;
  font-family: Jost;
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 32px;
  /* 160% */
}

.blog_card_info_text {
  height: 96px;
  align-self: stretch;

  overflow: hidden;
  color: #000;
  text-overflow: ellipsis;
  /* white-space: nowrap; */
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 300;
  line-height: 24px;
  /* 171.429% */
}

.tag_container {
  padding-left: 24px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.tag_componet {
  display: flex;
  padding: 4px 12px;
  justify-content: center;
  align-items: center;
  gap: 10px;

  border-radius: 24px;
  border: 1px solid rgba(129, 110, 252, 0.32);

  color: rgba(129, 110, 252, 1);
  font-family: Jost;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  /* 171.429% */

  cursor: pointer;
  transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
}

.tag_componet:hover {
  border: 1px solid rgba(129, 110, 252, 0.32);
  color: rgba(129, 110, 252, 0.65);
  transform: translateY(-4px);
}
</style>
