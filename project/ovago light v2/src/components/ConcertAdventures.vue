<script setup>
// ====== Importare biblioteca paralax ======

import { gsap } from "gsap"
import { ScrollTrigger } from "gsap/ScrollTrigger"
import { onMounted } from "vue"

gsap.registerPlugin(ScrollTrigger)


onMounted(() => {

  // gsap.from(".may_main_title", {
  //   scrollTrigger: {
  //     trigger: ".may_component",
  //     start: "top bottom",
  //     end: "center 60%",
  //     //  markers: true,
  //     scrub: true,
  //     // toggleActions: "restart pause reverse pause"
  //   },
  //   y: -240,
  //   opacity: 0,
  //   scale: 0.4,
  //   stagger: 0.1,
  //   fontWeight: 100,
  //   ease: 'power1.inOut'
  // })

  gsap.from(".may_parallax_dreapta", {
    scrollTrigger: {
      trigger: ".concert_container",
      start: "20% bottom",
      end: "110% bottom",
      // markers: true,
      scrub: true,
      // toggleActions: "restart pause reverse pause"
    },
    y: 32,
    x: 132,
    opacity: 0,
    scale: 0.8,
    stagger: 0.2,
    // ease:"back.inOut",
  })

  gsap.from(".may_parallax_stinga", {
    scrollTrigger: {
      trigger: ".concert_container",
      start: "20% bottom",
      end: "110% bottom",
      // markers: true,
      scrub: true,
      // toggleActions: "restart pause reverse pause"
    },
    y: 32,
    x: -132,
    opacity: 0,
    scale: 0.8,
    stagger: 0.2,
    // ease:"back.inOut",
  })

  gsap.from(".concert_bloc", {
    scrollTrigger: {
      trigger: ".concert_container",
      start: "20% bottom",
      end: "110% bottom",
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

  let tl = gsap.timeline({
    scrollTrigger: {
      trigger: ".concert_container",
      start: "20% bottom",
      end: "200% bottom",
      scrub: true,
      // markers: true
    }
  });

  tl.from(".may_parallax_stinga_big", {
    y: 32,
    x: -132,
    opacity: 0,
    scale: 0.8,
    stagger: 0.2,
  })
    .to(".may_parallax_stinga_big", {
      y: -80,
    });

  let rtl = gsap.timeline({
    scrollTrigger: {
      trigger: ".concert_container",
      start: "20% bottom",
      end: "200% bottom",
      scrub: true,
      // markers: true
    }
  });

  rtl.from(".may_parallax_dreapta_big", {
    y: 32,
    x: 132,
    opacity: 0,
    scale: 0.8,
    stagger: 0.2,
  })
    .to(".may_parallax_dreapta_big", {
      y: -80,
    });

})


</script>

<template>
  <div class="concert_container">

    <div class="concert_bloc">

      <div class="concert_title_main">
        Concert Adventures Await!
      </div>

      <div class="concert_title_description">
        Book your airplane tickets now to top concert venues—experience the music, excitement, and unforgettable
        destinations all in one trip!
      </div>

    </div>
    <div class="concert_card_wraper_8 may_parallax_dreapta">
      <div class="concert_card">
        <div class="concert_card_date">
          12 JUN
        </div>
        <div class="concert_card_imag_mic_strong card_imag_8">
        </div>
        <div class="concert_details_mic">
          <div class="details_title">
            Imagine Dragons
          </div>

          <div class="details_location">
            Frankfurt, Germany
          </div>

          <div class="details_price">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="black" />
            </svg>
            <div class="price_element">

              <div class="price_element_from">
                from
              </div>
              <div class="price_element_price">
                $450*
              </div>
            </div>
          </div>

        </div>


      </div>
    </div>

    <div class="concert_card_wraper_4 may_parallax_dreapta_big ">
      <div class="concert_card">
        <div class="concert_card_date">
          12 JUN
        </div>
        <div class="concert_card_imag card_imag_4">
        </div>
        <div class="concert_details">
          <div class="details_title">
            Imagine Dragons
          </div>

          <div class="details_location">
            Frankfurt, Germany
          </div>

          <div class="details_price">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="black" />
            </svg>
            <div class="price_element">

              <div class="price_element_from">
                from
              </div>
              <div class="price_element_price">
                $450*
              </div>
            </div>
          </div>

        </div>


      </div>
    </div>

    <div class="concert_card_wraper_1  may_parallax_stinga_big">
      <div class="concert_card">
        <div class="concert_card_date">
          12 JUN
        </div>
        <div class="concert_card_imag card_imag_1">
        </div>
        <div class="concert_details">
          <div class="details_title">
            Imagine Dragons
          </div>

          <div class="details_location">
            Frankfurt, Germany
          </div>

          <div class="details_price">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="black" />
            </svg>
            <div class="price_element">

              <div class="price_element_from">
                from
              </div>
              <div class="price_element_price">
                $450*
              </div>
            </div>
          </div>

        </div>


      </div>
    </div>

    <div class="concert_card_wraper_5 may_parallax_stinga">
      <div class="concert_card">
        <div class="concert_card_date">
          12 JUN
        </div>
        <div class="concert_card_imag_mic_strong card_imag_5">
        </div>
        <div class="concert_details_mic">
          <div class="details_title">
            Imagine Dragons
          </div>

          <div class="details_location">
            Frankfurt, Germany
          </div>

          <div class="details_price">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="black" />
            </svg>
            <div class="price_element">

              <div class="price_element_from">
                from
              </div>
              <div class="price_element_price">
                $450*
              </div>
            </div>
          </div>

        </div>


      </div>
    </div>

    <div class="concert_card_wraper_2  may_parallax_stinga_big">
      <div class="concert_card">
        <div class="concert_card_date">
          12 JUN
        </div>
        <div class="concert_card_imag_strong card_imag_2">
        </div>
        <div class="concert_details">
          <div class="details_title">
            Imagine Dragons
          </div>

          <div class="details_location">
            Frankfurt, Germany
          </div>

          <div class="details_price">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="black" />
            </svg>
            <div class="price_element">

              <div class="price_element_from">
                from
              </div>
              <div class="price_element_price">
                $450*
              </div>
            </div>
          </div>

        </div>


      </div>
    </div>

    <div class="concert_card_wraper_7 may_parallax_dreapta">
      <div class="concert_card">
        <div class="concert_card_date">
          12 JUN
        </div>
        <div class="concert_card_imag_mic_strong card_imag_7">
        </div>
        <div class="concert_details_mic">
          <div class="details_title">
            Imagine Dragons
          </div>

          <div class="details_location">
            Frankfurt, Germany
          </div>

          <div class="details_price">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="black" />
            </svg>
            <div class="price_element">

              <div class="price_element_from">
                from
              </div>
              <div class="price_element_price">
                $450*
              </div>
            </div>
          </div>

        </div>


      </div>
    </div>

    <div class="concert_card_wraper_3 may_parallax_dreapta_big ">
      <div class="concert_card">
        <div class="concert_card_date">
          12 JUN
        </div>
        <div class="concert_card_imag_strong card_imag_3">
        </div>
        <div class="concert_details">
          <div class="details_title">
            Imagine Dragons
          </div>

          <div class="details_location">
            Frankfurt, Germany
          </div>

          <div class="details_price">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="black" />
            </svg>
            <div class="price_element">

              <div class="price_element_from">
                from
              </div>
              <div class="price_element_price">
                $450*
              </div>
            </div>
          </div>

        </div>


      </div>
    </div>

    <div class="concert_card_wraper_6 may_parallax_stinga">
      <div class="concert_card">
        <div class="concert_card_date">
          12 JUN
        </div>
        <div class="concert_card_imag_mic_strong card_imag_6">
        </div>
        <div class="concert_details_mic">
          <div class="details_title">
            Imagine Dragons
          </div>

          <div class="details_location">
            Frankfurt, Germany
          </div>

          <div class="details_price">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <path
                d="M18.0961 19.4443L17.001 20.5394L13.1249 13.0131L8.75336 16.6719L9.43125 20.27L8.70122 21L6.58064 17.4194L3 15.2988L3.73003 14.5687L7.32806 15.2466L10.9869 10.8751L3.46062 6.99899L4.55567 5.90394L13.9071 7.95499L16.0972 5.76489C16.7031 5.15896 19.8809 2.24834 20.8163 3.18369C21.7517 4.11905 18.841 7.29692 18.2351 7.90284L16.045 10.0929L18.0961 19.4443Z"
                fill="black" />
            </svg>
            <div class="price_element">

              <div class="price_element_from">
                from
              </div>
              <div class="price_element_price">
                $450*
              </div>
            </div>
          </div>

        </div>


      </div>
    </div>

  </div>


</template>

<style scoped>
.concert_container {
  display: flex;
  margin: 320px 108px 0px 108px;
  height: 796px;

  justify-content: center;
  align-items: center;

  flex-direction: column;
  position: relative;
}

.concert_bloc {
  display: flex;
  width: 450px;
  flex-direction: column;
  align-items: center;
  gap: 16px;
}

.concert_title_main {
  align-self: stretch;

  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 32px;
  font-style: normal;
  font-weight: 500;
  line-height: 40px;
  /* 125% */
}

.concert_title_description {
  align-self: stretch;

  color: rgba(0, 0, 0, 0.56);
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  /* 150% */
  letter-spacing: 0.64px;
}

.concert_card_wraper_1 {
  display: inline-flex;
  align-items: center;
  position: absolute;
  top: 0px;
  left: 308px;
}

.concert_card_wraper_5 {
  display: inline-flex;
  align-items: center;
  position: absolute;
  top: 260px;
  left: 0px;
}

.concert_card_wraper_2 {
  display: inline-flex;
  align-items: center;
  position: absolute;
  bottom: 18px;
  left: 214px;
}

.concert_card_wraper_6 {
  display: inline-flex;
  align-items: center;
  position: absolute;
  bottom: 0px;
  left: 687px;
}

.concert_card_wraper_3 {
  display: inline-flex;
  align-items: center;
  position: absolute;
  bottom: 18px;
  right: 316px;
}

.concert_card_wraper_7 {
  display: inline-flex;
  align-items: center;
  position: absolute;
  bottom: 162px;
  right: 0px;
}

.concert_card_wraper_4 {
  display: inline-flex;
  align-items: center;
  position: absolute;
  top: 0px;
  right: 130px;
}

.concert_card_wraper_8 {
  display: inline-flex;
  align-items: center;
  position: absolute;
  top: 0px;
  right: 580px;
}

.concert_card {
  display: inline-flex;
  align-items: center;
  position: relative;

  cursor: pointer;
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
}

.concert_card:hover {
  transform: translateY(12px) scale(1.2);
}

.concert_card_imag {
  width: 288px;
  height: 288px;
  aspect-ratio: 1/1;
  border-radius: 40px;

  /* card_1 */
  box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.12);
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
}

.concert_card:hover .concert_card_imag {
  box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.12);
}

.concert_card_imag_mic {
  width: 200px;
  height: 200px;
  flex-shrink: 0;
  aspect-ratio: 1/1;
  border-radius: 24px;

  /* card_1 */
  box-shadow: 0px 8px 16px 0px rgba(93, 80, 180, 0.12);
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
}

.concert_card:hover .concert_card_imag_mic {
  box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.12);
}

.concert_card_imag_mic_strong {
  width: 200px;
  height: 200px;
  flex-shrink: 0;
  aspect-ratio: 1/1;
  border-radius: 24px;

  /* card_1 */
  box-shadow: 0px 8px 16px 0px rgba(33, 0, 93, 0.24);
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
}

.concert_card:hover .concert_card_imag_mic_strong {
  box-shadow: 0px 4px 4px 0px rgba(33, 0, 93, 0.24);
}

.concert_card_imag_strong {
  width: 288px;
  height: 288px;
  aspect-ratio: 1/1;
  border-radius: 40px;

  /* card_2 */
  box-shadow: 0px 8px 16px 0px rgba(33, 0, 93, 0.24);
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);

}

.concert_card:hover .concert_card_imag_strong {
  box-shadow: 0px 4px 4px 0px rgba(33, 0, 93, 0.24);
}

.card_imag_1 {
  background: url(/src/components/media/concert_1.jpg) lightgray 50% / cover no-repeat;
}

.card_imag_2 {
  background: url(/src/components/media/concert_2.jpg) lightgray 50% / cover no-repeat;
}

.card_imag_3 {
  background: url(/src/components/media/concert_3.jpg) lightgray 50% / cover no-repeat;
}

.card_imag_4 {
  background: url(/src/components/media/concert_4.jpg) lightgray 50% / cover no-repeat;
}

.card_imag_5 {
  background: url(/src/components/media/concert_5.jpg) lightgray 50% / cover no-repeat;
}

.card_imag_6 {
  background: url(/src/components/media/concert_6.jpg) lightgray 50% / cover no-repeat;
}

.card_imag_7 {
  background: url(/src/components/media/concert_7.jpg) lightgray 50% / cover no-repeat;
}

.card_imag_8 {
  background: url(/src/components/media/concert_8.jpg) lightgray 50% / cover no-repeat;
}

.concert_card_date {
  display: flex;
  transform: rotate(-15deg);
  padding: 8px 24px;
  justify-content: center;
  align-items: center;
  gap: 10px;

  position: absolute;
  left: 32px;
  top: -30px;

  border-radius: 32px;
  background: rgba(255, 255, 255, 0.48);
  backdrop-filter: blur(16px);

  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 24px;
  /* 150% */
  letter-spacing: 0.64px;
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
}

.concert_card:hover .concert_card_date {
  transform: rotate(-20deg) translateY(8px);
}

.concert_details {
  display: flex;
  padding: 24px;
  flex-direction: column;
  align-items: center;
  gap: 8px;

  position: absolute;
  left: 50%;
  top: 82%;

  transform: translateX(-50%);

  border-radius: 32px;
  background: rgba(255, 255, 255, 0.24);
  backdrop-filter: blur(16px);
  z-index: 2;
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
  opacity: 0;
}



.concert_card:hover .concert_details {
  transform: translateX(-50%) translateY(-24px);
  opacity: 1;
}

.concert_details_mic {
  display: flex;
  padding: 12px;
  flex-direction: column;
  align-items: center;
  gap: 8px;

  position: absolute;
  left: 50%;
  top: 82%;

  transform: translateX(-50%);

  border-radius: 24px;
  background: rgba(255, 255, 255, 0.24);
  backdrop-filter: blur(16px);
  z-index: 2;
  transition: all 800ms cubic-bezier(0.3, 0, 0, 1);
  opacity: 0;
}



.concert_card:hover .concert_details_mic {
  transform: translateX(-50%) translateY(-24px);
  opacity: 1;
}



.details_title {
  color: #000;
  font-family: Jost;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  /* 133.333% */
}

.details_location {
  color: rgba(0, 0, 0, 0.48);
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
  /* 150% */
}

.details_price {
  display: flex;
  align-items: center;
  gap: 8px;
}

.price_element {
  display: flex;
  align-items: baseline;
  gap: 8px;
}

.price_element_from {
  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 32px;
  /* 200% */
}

.price_element_price {
  color: #000;
  text-align: center;
  font-family: Jost;
  font-size: 24px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}
</style>
