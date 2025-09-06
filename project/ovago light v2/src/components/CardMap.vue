
<script setup>

import { defineProps } from 'vue';
  

defineProps(['imagSrc', 'titleSrc', 'priceSrc']);

</script>

<template>

  <div class="card_component">
    <div class="imagine_card" :style="{ backgroundImage: `url(${imagSrc})`, backgroundPosition: '50%',  }"></div>

    <div class="info_card">

      <div class="titlu_detalii">
        <div class="titlu_card">
          {{ titleSrc }}
        </div>

        <div class="detalii_trip">
          Round Trip, Economy, 1 pass
          
        </div>
      </div>

      <div class="container_pret">
        <div class="from">
          from
        </div>

        <div class="pretul">
          {{ priceSrc }}
        </div>
      </div>

    </div>
  </div>







</template>

<style scoped>

  .card_component{
    display: flex;
    width: 340px;
    padding-bottom: 32px;
    flex-direction: column;
    align-items: flex-start;
    gap: 24px;

    border-radius: 32px;
    background: #FFF;
    box-shadow: 0px 12px 16px 0px rgba(93, 80, 180, 0.16);

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }
  .card_component:hover{
    box-shadow: 0px 4px 4px 0px rgba(93, 80, 180, 0.20);
  }

  .info_card{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 32px;
    align-self: stretch;
  }
    .imagine_card{
      display: flex;
      width: 340px;
      height: 384px;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      border-radius: 32px;
      /* background: url(/src/media/paris_card.png) lightgray 50% / cover no-repeat;  */
    }

    .titlu_detalii{
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      gap: 12px;
      align-self: stretch;
    }
      .titlu_card{
        align-self: stretch;

        color: #000;
        text-align: center;
        font-family: Jost;
        font-size: 24px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
      }

      .detalii_trip{
        align-self: stretch;

        color: rgba(0, 0, 0, 0.48);
        text-align: center;
        font-family: Jost;
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: 16px; /* 114.286% */
      }

      .container_pret{
        display: flex;
        padding-right: 36px;
        align-items: center;
        gap: 8px;
      }

      .pretul{
        color: #000;
        text-align: center;
        font-family: Jost;
        font-size: 24px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
      }

      .from{
        color: rgba(0, 0, 0, 0.48);
        text-align: center;
        font-family: Jost;
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: 16px; /* 114.286% */
      }


</style>