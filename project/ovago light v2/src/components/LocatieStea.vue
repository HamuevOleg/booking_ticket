<script setup>

  import { defineProps } from 'vue';
  

  const props = defineProps({
    imageSrc: {
      type: String,
      required: true
    }
  });



</script>

<template>

  <div class="grupare_stea_pin">

    <div class="pin_imagine" :style="{ backgroundImage: `url(${imageSrc})`, backgroundPosition: '50%',  }"></div>

      <svg class="pin" xmlns="http://www.w3.org/2000/svg" width="42" height="46" viewBox="0 0 42 46" fill="none">
        <g filter="url(#filter0_d_90_1717)">
          <path d="M20.9998 30L33.1242 0H8.87549L20.9998 30Z" fill="white"/>
        </g>
        <defs>
          <filter id="filter0_d_90_1717" x="0.875488" y="0" width="40.2485" height="46" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
            <feFlood flood-opacity="0" result="BackgroundImageFix"/>
            <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
            <feOffset dy="8"/>
            <feGaussianBlur stdDeviation="4"/>
            <feComposite in2="hardAlpha" operator="out"/>
            <feColorMatrix type="matrix" values="0 0 0 0 0.364706 0 0 0 0 0.313726 0 0 0 0 0.705882 0 0 0 0.16 0"/>
            <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_90_1717"/>
            <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_90_1717" result="shape"/>
          </filter>
        </defs>
      </svg>

      <div class="gruparea_stea">

        <svg class="cercul" xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 12 12" fill="none">
          <circle cx="6" cy="6" r="6" fill="#816EFC"/>
        </svg>

        <svg class="stea" xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none">
          <path d="M18 36L11.25 24.75L0 18L11.25 11.25L18 0L24.75 11.25L36 18L24.75 24.75L18 36Z" fill="#816EFC" fill-opacity="0.16"/>
        </svg>

      </div>

  </div>

</template>

<style scoped>

  /* Stea */

  .grupare_stea_pin{

    display: flex;
    flex-direction: column;
    gap: 24px;

    align-items: center;
    align-content: center;
    position: relative;

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);

  }

    .grupare_stea_pin:hover{
      gap: 40px;
      transform: translateY(-16px);
    } 

    .pin_imagine{
      width: 72px;
      height: 72px;

      border-radius: 72px;
      border: 8px solid #FFF;
      /* background: url(/src/media/paris.png) lightgray 50% / cover no-repeat; */

      /* map point */
      box-shadow: 0px 8px 8px 0px rgba(93, 80, 180, 0.16);

      cursor: pointer;
      transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
    }

    .grupare_stea_pin:hover .pin_imagine{

      transform: scale(1.24);

    }


  .pin{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, 10%);
  }

  .gruparea_stea{
    width: 50px;
    height: 50px;
    position: relative;

  }

  .cercul{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  .stea{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .grupare_stea_pin:hover .stea{

    width: 50px;
    height: 50px;

  }

</style>