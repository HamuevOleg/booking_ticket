<script setup>

</script>

<template>      
  <div class="containerul_taburi_cautare">

    <div class="tab_elemet">
      <div class="tab_label">
        One-way          
      </div> 
      <div class="linie_tab_default"></div>
    </div>

    <div class="tab_elemet">
      <div class="tab_label label_default">
        Round-trip          
      </div> 
      <div class="linie_tab"></div>
    </div>

    <div class="tab_elemet">
      <div class="tab_label">
        Multi-city          
      </div> 
      <div class="linie_tab_default"></div>
    </div>


  </div>

</template>

<style scoped>


  /* taburile */

  .containerul_taburi_cautare{
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
    color: rgba(0, 0, 0, 0.48);
    font-family: Jost;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 16px; /* 133.333% */
    letter-spacing: 2.16px;
    text-transform: uppercase;

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

</style>