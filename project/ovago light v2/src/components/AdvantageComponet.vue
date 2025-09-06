<script setup>

  // ====== Importare biblioteca paralax ======

  import { gsap } from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  import { onMounted } from "vue"

  gsap.registerPlugin(ScrollTrigger)


  onMounted(() => {

    gsap.to(".parallax_money", {
      scrollTrigger:{
        trigger: ".grupa_avantaje",
        start: "top bottom",
        // end: "center center",
        // markers: true,
        // scrub: true,
        toggleActions: "restart pause reverse pause"
      },
      rotation:360,
      duration:3,
      y:0,
      x:0,
  
    })

    gsap.from(".container_imagin", {
      scrollTrigger:{
        trigger: ".grupa_avantaje",
        start: "top bottom",
        end: "+=700",
        // markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
      },
      y:-160,
      rotate:30,
      opacity:0,
      scale:0.4,
      stagger:0.2,
      ease:"back.inOut",
    })

    gsap.from(".imagine_parallax_prim", {
      scrollTrigger:{
        trigger: ".grupa_avantaje",
        start: "top bottom",
        end: "+=700",
        // markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
      },
      x:200,
      ease:"back.inOut",
    })

    gsap.from(".imagine_parallax_sec", {
      scrollTrigger:{
        trigger: ".grupa_avantaje",
        start: "top bottom",
        end: "+=700",
        // markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
      },
      x:-400,
      ease:"back.inOut",
    })

  })


</script>

<template>

  <div class="grupa_avantaje">

    <div class="avantaj_componet">

      <div class="container_imagin imagine_parallax_prim">

        <svg class="imagine_fata" xmlns="http://www.w3.org/2000/svg" width="80" height="80" viewBox="0 0 80 80" fill="none">
          <path d="M60.8332 35.0556C60.8332 33.951 61.7287 33.0556 62.8332 33.0556H64.841C69.5311 33.0556 73.3332 36.8576 73.3332 41.5478V51.23C73.3332 55.9201 69.5311 59.7222 64.841 59.7222H62.8332C61.7287 59.7222 60.8332 58.8268 60.8332 57.7222V35.0556Z" fill="white"/>
          <path d="M18.3332 35.0556C18.3332 33.951 17.4378 33.0556 16.3332 33.0556H15.1588C10.4686 33.0556 6.66656 36.8576 6.66656 41.5478V51.23C6.66656 55.9201 10.4686 59.7222 15.1588 59.7222H16.3332C17.4378 59.7222 18.3332 58.8268 18.3332 57.7222V35.0556Z" fill="white"/>
          <path fill-rule="evenodd" clip-rule="evenodd" d="M1.94434 38.0556C1.94434 17.0381 18.9824 0 39.9999 0C61.0174 0 78.0555 17.0381 78.0555 38.0556V54.0825C78.0555 54.8496 77.4336 55.4714 76.6666 55.4714C75.8995 55.4714 75.2777 54.8496 75.2777 54.0825V38.0556C75.2777 18.5722 59.4833 2.77778 39.9999 2.77778C20.5165 2.77778 4.72211 18.5722 4.72211 38.0556V50.4637C4.72211 63.0942 14.9612 73.3333 27.5918 73.3333C28.3588 73.3333 28.9807 73.9552 28.9807 74.7222C28.9807 75.4893 28.3588 76.1111 27.5918 76.1111C13.4271 76.1111 1.94434 64.6284 1.94434 50.4637V38.0556Z" fill="white"/>
          <path d="M37.4999 74.3056C37.4999 77.2971 35.0748 79.7222 32.0832 79.7222C29.0917 79.7222 26.6666 77.2971 26.6666 74.3056C26.6666 71.314 29.0917 68.8889 32.0832 68.8889C35.0748 68.8889 37.4999 71.314 37.4999 74.3056Z" fill="white"/>
        </svg>


        <svg class="imagine_fundal" xmlns="http://www.w3.org/2000/svg" width="200" height="200" viewBox="0 0 200 200" fill="none">
          <rect width="200" height="200" rx="100" fill="url(#paint0_linear_311_6518)" fill-opacity="0.7"/>
          <defs>
          <linearGradient id="paint0_linear_311_6518" x1="100" y1="0" x2="100" y2="200" gradientUnits="userSpaceOnUse">
          <stop stop-color="#AB9FFF"/>
          <stop offset="1" stop-color="#FFDEF3"/>
          </linearGradient>
          </defs>
        </svg>

      </div>

      <div class="avantaj_info">

        <div class="titlu_avantaj">
          Assistance 24/7
        </div>

        <div class="info_avantaj">
          We’re always here for you – reach us 24 hours a day, 7 days a week.
        </div>
      </div>

    </div>

    <div class="avantaj_componet">

      <div class="container_imagin imagine_parallax_prim">

        <svg class="imagine_fata" xmlns="http://www.w3.org/2000/svg" width="80" height="80" viewBox="0 0 80 80" fill="none">
          <path d="M40.0082 76.7C39.456 76.7 39.0082 76.2523 39.0082 75.7V5.6333C39.0082 5.08101 39.456 4.6333 40.0082 4.6333H40.786C41.3383 4.6333 41.786 5.08102 41.786 5.6333V75.7C41.786 76.2523 41.3383 76.7 40.786 76.7H40.0082ZM39.9333 67.96C35.9467 67.96 32.1133 67.3211 28.4333 66.0433C25.3997 64.9324 22.9376 63.5715 21.047 61.9606C20.3949 61.4049 20.2613 60.4697 20.6498 59.7062L20.9921 59.0333C21.6033 57.8321 23.2131 57.563 24.3095 58.3468C25.8579 59.4538 27.6926 60.4348 29.8133 61.29C33.0333 62.5166 36.4067 63.13 39.9333 63.13C43.3067 63.13 46.0411 62.7211 48.1367 61.9033C50.2833 61.0344 51.8422 59.8844 52.8133 58.4533C53.8356 57.0222 54.3467 55.4377 54.3467 53.7C54.3467 51.6044 53.7333 49.9177 52.5067 48.64C51.3311 47.3622 49.7722 46.3655 47.83 45.65C45.8878 44.8833 43.7411 44.2189 41.39 43.6566C39.0389 43.0944 36.6878 42.5066 34.3367 41.8933C31.9856 41.2289 29.8133 40.36 27.82 39.2866C25.8778 38.2133 24.2933 36.8077 23.0667 35.07C21.8911 33.2811 21.3033 30.9555 21.3033 28.0933C21.3033 25.4355 21.9933 23.0077 23.3733 20.81C24.8044 18.5611 26.9767 16.7722 29.89 15.4433C32.8033 14.0633 36.5344 13.3733 41.0833 13.3733C44.0989 13.3733 47.0889 13.8077 50.0533 14.6766C52.4083 15.3263 54.5053 16.1856 56.3442 17.2546C57.1645 17.7314 57.4545 18.7533 57.0843 19.6269L56.7453 20.4269C56.2562 21.5813 54.8388 22.0008 53.7361 21.4042C52.0483 20.4911 50.284 19.7819 48.4433 19.2766C45.8878 18.5611 43.4089 18.2033 41.0067 18.2033C37.7867 18.2033 35.1289 18.6377 33.0333 19.5066C30.9378 20.3755 29.3789 21.5511 28.3567 23.0333C27.3856 24.4644 26.9 26.1 26.9 27.94C26.9 30.0355 27.4878 31.7222 28.6633 33C29.89 34.2777 31.4744 35.2744 33.4167 35.99C35.41 36.7055 37.5822 37.3444 39.9333 37.9066C42.2844 38.4689 44.61 39.0822 46.91 39.7466C49.2611 40.4111 51.4078 41.28 53.35 42.3533C55.3433 43.3755 56.9278 44.7555 58.1033 46.4933C59.33 48.2311 59.9433 50.5055 59.9433 53.3166C59.9433 55.9233 59.2278 58.3511 57.7967 60.6C56.3656 62.7977 54.1678 64.5866 51.2033 65.9666C48.29 67.2955 44.5333 67.96 39.9333 67.96Z" fill="white"/>
        </svg>

        <div class="parallax_money">

          <svg class="imagine_fundal" xmlns="http://www.w3.org/2000/svg" width="200" height="200" viewBox="0 0 200 200" fill="none">
            <path d="M195.456 107.876C201.52 104.245 201.513 95.4567 195.444 91.835L142.522 60.2566C141.21 59.4735 140.11 58.3806 139.318 57.0735L107.474 4.50303C103.826 -1.51891 95.0817 -1.49663 91.4647 4.54383L60.115 56.8985C59.3242 58.2193 58.2193 59.3242 56.8986 60.115L4.54383 91.4647C-1.49662 95.0817 -1.51891 103.826 4.50303 107.474L57.0735 139.318C58.3806 140.11 59.4735 141.21 60.2566 142.522L91.835 195.444C95.4567 201.513 104.245 201.52 107.876 195.456L139.473 142.689C140.264 141.369 141.369 140.264 142.689 139.473L195.456 107.876Z" fill="url(#paint0_linear_311_6521)" fill-opacity="0.7"/>
            <defs>
              <linearGradient id="paint0_linear_311_6521" x1="154.357" y1="45.3339" x2="45.3339" y2="154.357" gradientUnits="userSpaceOnUse">
                <stop stop-color="#AB9FFF"/>
                <stop offset="1" stop-color="#FFDEF3"/>
              </linearGradient>
            </defs>
          </svg>

        </div>

        

      </div>

      <div class="avantaj_info">

        <div class="titlu_avantaj">
          Lowest Price Guarantee
        </div>

        <div class="info_avantaj">
          Book with confidence - you’ll always get the best price.
        </div>
      </div>

    </div>

    <div class="avantaj_componet">

      <div class="container_imagin imagine_parallax_sec">
        <svg class="imagine_fata" xmlns="http://www.w3.org/2000/svg" width="80" height="80" viewBox="0 0 80 80" fill="none">
          <path d="M27.7641 62.8502C27.5512 63.9983 28.4996 65 29.6672 65H53.6668C54.8344 65 55.7828 63.9983 55.5699 62.8502C55.3593 61.7145 55.003 60.6125 54.3362 59.5891C53.2543 57.9285 42.9951 54.0233 42.9951 54.0233C42.9951 54.0233 42.6063 40.3331 42.5524 37.7778C42.5286 36.6506 44.184 35.1362 46.2603 33.2367C48.2403 31.4253 50.6031 29.2637 52.2574 26.7539C53.0324 25.578 52.0989 24.1667 50.6906 24.1667H32.6433C31.2351 24.1667 30.3015 25.578 31.0766 26.7539C32.7309 29.2637 35.0937 31.4253 37.0737 33.2367C39.1499 35.1362 40.8053 36.6506 40.7816 37.7778C40.7277 40.3331 40.3389 54.0233 40.3389 54.0233C40.3389 54.0233 30.0797 57.9285 28.9978 59.5891C28.331 60.6125 27.9747 61.7145 27.7641 62.8502Z" fill="white"/>
          <path fill-rule="evenodd" clip-rule="evenodd" d="M61.667 9.5C61.667 8.39543 60.7716 7.5 59.667 7.5H23.667C22.5624 7.5 21.667 8.39543 21.667 9.5V11.8055C21.667 12.1891 21.9779 12.5 22.3615 12.5V12.5C22.745 12.5 23.0554 12.8112 23.0605 13.1947C23.1501 19.9877 24.5526 24.7504 26.4856 28.2821C28.4688 31.9056 30.9628 34.1357 32.8772 35.8477L32.9052 35.8727C33.9357 36.7942 34.7113 37.4942 35.2497 38.1891C35.7567 38.8437 35.9726 39.3949 35.9726 40C35.9726 40.6051 35.7567 41.1563 35.2497 41.8109C34.7113 42.5058 33.9357 43.2058 32.9052 44.1273L32.8772 44.1523C30.9628 45.8642 28.4688 48.0944 26.4856 51.7179C24.5526 55.2496 23.1501 60.0123 23.0605 66.8053C23.0554 67.1888 22.745 67.5 22.3615 67.5V67.5C21.9779 67.5 21.667 67.8109 21.667 68.1945V70.5C21.667 71.6046 22.5624 72.5 23.667 72.5H59.667C60.7716 72.5 61.667 71.6046 61.667 70.5V68.1944C61.667 67.8109 61.3561 67.5 60.9726 67.5V67.5C60.589 67.5 60.2786 67.1888 60.2736 66.8053C60.1839 60.0123 58.7815 55.2496 56.8485 51.7179C54.8653 48.0944 52.3713 45.8642 50.4568 44.1523L50.4288 44.1273C49.3983 43.2058 48.6228 42.5058 48.0844 41.8109C47.5773 41.1563 47.3615 40.6051 47.3615 40C47.3615 39.3949 47.5773 38.8437 48.0844 38.1891C48.6228 37.4942 49.3983 36.7942 50.4288 35.8727L50.4568 35.8477C52.3713 34.1357 54.8653 31.9056 56.8485 28.2821C58.7815 24.7504 60.1839 19.9877 60.2736 13.1947C60.2786 12.8112 60.589 12.5 60.9726 12.5V12.5C61.3561 12.5 61.667 12.1891 61.667 11.8056V9.5ZM28.9223 26.9485C27.4965 24.3436 26.3324 20.8541 25.9594 15.9446C25.874 14.821 26.7841 13.8889 27.911 13.8889H55.4231C56.5499 13.8889 57.46 14.821 57.3747 15.9446C57.0017 20.8541 55.8375 24.3436 54.4118 26.9485C52.6677 30.1351 50.4834 32.0975 48.5772 33.8021L48.5152 33.8576C47.5621 34.7097 46.5989 35.5709 45.8885 36.488C45.1312 37.4654 44.5837 38.5996 44.5837 40C44.5837 41.4004 45.1312 42.5346 45.8884 43.512C46.5989 44.4291 47.5621 45.2903 48.5152 46.1425L48.5772 46.1979C50.4834 47.9025 52.6677 49.8649 54.4118 53.0515C55.8375 55.6564 57.0017 59.1459 57.3747 64.0554C57.46 65.179 56.5499 66.1111 55.4231 66.1111H27.911C26.7841 66.1111 25.874 65.179 25.9594 64.0554C26.3324 59.1459 27.4965 55.6564 28.9223 53.0515C30.6664 49.8649 32.8507 47.9025 34.7568 46.1979L34.8189 46.1425C35.7719 45.2903 36.7351 44.4291 37.4456 43.512C38.2028 42.5346 38.7504 41.4004 38.7504 40C38.7504 38.5996 38.2028 37.4654 37.4456 36.488C36.7351 35.5709 35.772 34.7097 34.8189 33.8576L34.7568 33.8021C32.8507 32.0975 30.6664 30.1351 28.9223 26.9485Z" fill="white"/>
        </svg>

        <svg class="imagine_fundal" xmlns="http://www.w3.org/2000/svg" width="200" height="200" viewBox="0 0 200 200" fill="none">
          <rect width="200" height="200" rx="100" fill="url(#paint0_linear_311_6519)" fill-opacity="0.7"/>
          <defs>
          <linearGradient id="paint0_linear_311_6519" x1="200" y1="100" x2="0" y2="100" gradientUnits="userSpaceOnUse">
          <stop stop-color="#AB9FFF"/>
          <stop offset="1" stop-color="#FFDEF3"/>
          </linearGradient>
          </defs>
        </svg>
      </div>

      <div class="avantaj_info">

        <div class="titlu_avantaj">
          Buy Now - Pay Later
        </div>

        <div class="info_avantaj">
          Book your once-in-a-lifetime travel now and pay for it safely over time.
        </div>
      </div>

    </div>

    <div class="avantaj_componet">

      <div class="container_imagin imagine_parallax_sec">
        <svg class="imagine_fata" xmlns="http://www.w3.org/2000/svg" width="80" height="80" viewBox="0 0 80 80" fill="none">
          <path d="M23.9139 38.0809C23.1328 37.2999 23.1328 36.0336 23.9138 35.2525L25.2521 33.9143C26.0331 33.1332 27.2995 33.1332 28.0805 33.9143L35.2521 41.0858C36.0331 41.8669 37.2995 41.8669 38.0805 41.0858L51.9188 27.2476C52.6998 26.4666 53.9661 26.4666 54.7472 27.2476L56.0854 28.5858C56.8665 29.3669 56.8665 30.6332 56.0854 31.4143L38.0805 49.4192C37.2995 50.2002 36.0331 50.2002 35.2521 49.4192L23.9139 38.0809Z" fill="white"/>
          <path fill-rule="evenodd" clip-rule="evenodd" d="M72.6366 13.563C72.6028 12.9687 72.1939 12.462 71.6202 12.3034L40.5326 3.70649C40.1837 3.61003 39.8153 3.61003 39.4664 3.7065L8.37885 12.3034C7.8051 12.462 7.39625 12.9687 7.3624 13.563V13.563C6.36351 31.0967 6.92478 44.0228 11.5393 53.959C16.205 64.0056 24.8929 70.7668 39.5078 76.299V76.299C39.8246 76.419 40.1744 76.419 40.4912 76.299V76.299C55.1061 70.7668 63.794 64.0056 68.4598 53.959C73.0743 44.0228 73.6355 31.0967 72.6366 13.563V13.563ZM10.0061 16.1526C10.0485 15.2943 10.6387 14.5605 11.467 14.3314L39.4664 6.58853C39.8153 6.49206 40.1837 6.49206 40.5326 6.58853L68.5321 14.3314C69.3604 14.5605 69.9505 15.2943 69.9929 16.1526C70.7953 32.402 70.032 43.9787 65.9404 52.789C61.8206 61.66 54.2149 67.9368 40.7192 73.2343C40.2589 73.4149 39.7402 73.4149 39.2799 73.2343C25.7841 67.9368 18.1784 61.66 14.0586 52.789C9.96703 43.9787 9.20371 32.402 10.0061 16.1526Z" fill="white"/>
        </svg>

        <svg class="imagine_fundal" xmlns="http://www.w3.org/2000/svg" width="183" height="182" viewBox="0 0 183 182" fill="none">
          <path d="M182.227 29.9433C186.646 12.336 170.672 -3.613 153.072 0.832533L97.7009 14.8182C93.8955 15.7793 89.9125 15.7926 86.1008 14.8567L30.7004 1.25407C13.139 -3.05782 -2.70203 12.8641 1.69932 30.4033L15.4398 85.1585C16.4021 88.9934 16.4021 93.0066 15.4398 96.8415L1.69932 151.597C-2.70203 169.136 13.139 185.058 30.7004 180.746L86.1008 167.143C89.9125 166.207 93.8955 166.221 97.7009 167.182L153.072 181.167C170.672 185.613 186.646 169.664 182.227 152.057L168.372 96.8415C167.409 93.0066 167.409 88.9934 168.372 85.1585L182.227 29.9433Z" fill="url(#paint0_linear_311_6520)" fill-opacity="0.7"/>
          <defs>
            <linearGradient id="paint0_linear_311_6520" x1="92" y1="-9" x2="92" y2="191" gradientUnits="userSpaceOnUse">
              <stop stop-color="#AB9FFF"/>
              <stop offset="1" stop-color="#FFDEF3"/>
            </linearGradient>
          </defs>
        </svg>
      </div>

      <div class="avantaj_info">

        <div class="titlu_avantaj">
          Secure Payment
        </div>

        <div class="info_avantaj">
          With our safe payment system, your data security is guaranteed.
        </div>
      </div>

    </div>
                

  </div>


</template>
  

<style scoped>

  .parallax_money{
    width: 265px;
    height: 265px;
    position: relative;
  }

  .container_imagin{
    position: relative;
    width: 265px;
    height: 265px;
  }

  .imagine_fundal{
    position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
  }

  .imagine_fata{
    position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      z-index: 4;
  }

  .grupa_avantaje{
    margin-top: 320px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0px 212px;
    position: relative;
  }

  .avantaj_componet{
    display: flex;
    width: 320px;
    flex-direction: column;
    align-items: center;
    gap: 48px;
    flex-shrink: 0;
  }

  .avantaj_info{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 24px;
    align-self: stretch;
  }

  .titlu_avantaj{
    color: #000;
    text-align: center;
    font-family: Jost;
    font-size: 24px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;

    align-self: stretch;
  }

  .info_avantaj{
    color: rgba(0, 0, 0, 0.56);
    text-align: center;
    font-family: Jost;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 24px; /* 150% */
    letter-spacing: 0.64px;

    align-self: stretch;
  }


</style>
