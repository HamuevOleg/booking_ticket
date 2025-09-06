<script setup>

  // ====== Importare biblioteca paralax ======

  import { gsap, } from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  import { onMounted } from "vue"

  gsap.registerPlugin(ScrollTrigger)


  onMounted(() => {

    gsap.set(".card_paralax", {
      y:240,
      x:240,
      scale:0.3,
      opacity:-1
    })

    gsap.to(".card_paralax", {
      scrollTrigger:{
        trigger: ".inspiratie_component",
        start: "top bottom",
        end: "center center",
        // markers: true,
        scrub: true,
        // toggleActions: "restart pause reverse pause"
        
      },
      y:0,
      x:0,
      ease: 'none',
      stagger: 0.1,
      scale:1,
      opacity:1,
      // ease:"back.inOut(1)",
    })
    

    gsap.from(".inspir_parallax", {
      scrollTrigger: {
        trigger: ".inspiratie_component",
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

  <div class="inspiratie_component">

    <div class="titlu_taburi">
      <div class="titlu_inspiration inspir_parallax">
        Inspiration for your next journey
      </div>

      <div class="containerul_taburi inspir_parallax">

        <div class="tab_elemet">
          <div class="tab_label">
            Beach Holiday          
          </div> 
          <div class="linie_tab_default"></div>
        </div>

        <div class="tab_elemet">
          <div class="tab_label">
            Winter Activities          
          </div> 
          <div class="linie_tab_default"></div>
        </div>

        <div class="tab_elemet">
          <div class="tab_label label_default ">
            Adventure Vacations          
          </div> 
          <div class="linie_tab"></div>
        </div>

        <div class="tab_elemet">
          <div class="tab_label ">
            Exotic Getaways          
          </div> 
          <div class="linie_tab_default"></div>
        </div>

        <div class="tab_elemet ">
          <div class="tab_label ">
            Romantic Vacations          
          </div> 
          <div class="linie_tab_default"></div>
        </div>

      </div>

    </div>

    <div class="grupa_grile">

      <div class="grila_1 card_paralax">
        <div class="grila_1_interior_imag" >
          <div class="info_container_imag_1">

            <div class="info_title">
              Ibiza
            </div>

            <div class="price_container">

              <div class="from_text">
                from
              </div>

              <div class="price_text">
                $450*
              </div>

            </div>

          </div>
        </div>
        <div class="grila_1_interior_grupa card_paralax">
          <div class="grila_1_interior_grupa_1">

            <div class="info_container_imag_2">

              <div class="info_title">
                London
              </div>

              <div class="price_container">

                <div class="from_text">
                  from
                </div>

                <div class="price_text">
                  $1800*
                </div>

              </div>

            </div>

          </div>
          <div class="grila_1_interior_grupa_2">

            <div class="info_container_imag_3">

              <div class="info_title">
                Zürich
              </div>

              <div class="price_container">

                <div class="from_text">
                  from
                </div>

                <div class="price_text">
                  $880*
                </div>

              </div>

            </div>

          </div>
        </div>
      </div>

      <div class="grila_2_cont card_paralax">

        <div class="grila_2">

          <div class="info_container">

            <div class="info_title">
              Paris
            </div>

            <div class="price_container">

              <div class="from_text">
                from
              </div>

              <div class="price_text">
                $450*
              </div>

            </div>
          
          </div>

        </div>
      </div>

      <div class="grila_3 card_paralax">
        <div class="grila_3_interior_1">

          <div class="info_container_imag_5">

            <div class="info_title">
              Santorini
            </div>

            <div class="price_container">

              <div class="from_text">
                from
              </div>

              <div class="price_text">
                $690*
              </div>

            </div>

          </div>

        </div>
        <div class="grila_3_interior_2">

          <div class="info_container_imag_6">

            <div class="info_title">
              Carpathian
            </div>

            <div class="price_container">

              <div class="from_text">
                from
              </div>

              <div class="price_text">
                $690*
              </div>

            </div>

          </div>

        </div>
      </div>
    </div>

  </div>







 
</template>

<style scoped>

  .inspiratie_component{
    margin-top:220px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 64px;

  }

  .titlu_taburi{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 32px;
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


  .grupa_grile{
    display: flex;
    gap: 40px;
    padding: 0 132px;
    align-items: center;
    position: relative;
  }

  /* grila 1 */

  .grila_1{
    display: flex;
    flex-direction: column;
    gap: 40px;

    width: 600px;
    height: 804px;
  }

  .grila_1_interior_imag{
    border-radius: 48px;
    flex-shrink: 0;

    width: 600px;
    height: 382px;

  
    overflow: hidden; 
    position: relative; 

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

    .grila_1_interior_imag::before{

      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: inherit;

      background: url(/src/components/media/spania.jpg) rgb(255, 255, 255) 50% / cover no-repeat;

      background-size: 100%; 
      transition: all 800ms cubic-bezier(0.3, 0, 0, 1); 

    }

    .grila_1_interior_imag:hover::before{
      background-size: 108%; 

    }

    .info_container_imag_1{
      position: absolute;
      bottom: 12px;
      left: 50%;
      transform: translate(-50%, 0);

      display: flex;
      width: 228px;
      padding: 23px 16px;
      justify-content: space-between;
      align-items: baseline;


    border-radius: 32px;
    /* border: 1px solid rgba(255, 255, 255, 0.24); */
    background: rgba(104, 97, 155, 0.08);
    backdrop-filter: blur(16px);


    opacity: 1;
    transition: all 800ms cubic-bezier(0.3, 0, 0, 1);

  }

  .grila_1_interior_imag:hover .info_container_imag_1 {
    opacity: 1;
    transform: translate(-50%, -16px);
  }

  .grila_1_interior_grupa{
    display: flex;
    gap: 32px;
    flex: 1;
  }

  .grila_1_interior_grupa_1{
    border-radius: 48px;
    flex-shrink: 0;

    width: 284px;
    height: 382px;

  
    overflow: hidden; 
    position: relative; 

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }
  .grila_1_interior_grupa_1::before{

    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/london.jpg) rgb(255, 255, 255) 50% / cover no-repeat;

    background-size: 100%; 
    transition: all 800ms cubic-bezier(0.3, 0, 0, 1); 

  }

  .grila_1_interior_grupa_1:hover::before{
    background-size: 108%; 
  }

  .info_container_imag_2{
      position: absolute;
      bottom: 12px;
      left: 50%;
      transform: translate(-50%, 0);

      display: flex;
      width: 228px;
      padding: 23px 16px;
      justify-content: space-between;
      align-items: baseline;

      border-radius: 32px;
      /* border: 1px solid rgba(255, 255, 255, 0.24); */
      background: rgba(104, 97, 155, 0.08);
      backdrop-filter: blur(16px);


      opacity: 1;
      transition: all 800ms cubic-bezier(0.3, 0, 0, 1);

    }

    .grila_1_interior_grupa_1:hover .info_container_imag_2 {
      opacity: 1;
      transform: translate(-50%, -16px);
    }

  .grila_1_interior_grupa_2{
    border-radius: 48px;
    flex-shrink: 0;

    width: 284px;
    height: 382px;

  
    overflow: hidden; 
    position: relative; 

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .grila_1_interior_grupa_2::before{

    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/germania.jpg) rgb(255, 255, 255) 50% / cover no-repeat;

    background-size: 100%; 
    transition: all 800ms cubic-bezier(0.3, 0, 0, 1); 

  }

  .grila_1_interior_grupa_2:hover::before{
    background-size: 108%; 
  }

  .info_container_imag_3{
    position: absolute;
      bottom: 12px;
      left: 50%;
      transform: translate(-50%, 0);

      display: flex;
      width: 228px;
      padding: 23px 16px;
      justify-content: space-between;
      align-items: baseline;

      border-radius: 32px;
      /* border: 1px solid rgba(255, 255, 255, 0.24); */
      background: rgba(104, 97, 155, 0.08);
      backdrop-filter: blur(16px);


      opacity: 1;
      transition: all 800ms cubic-bezier(0.3, 0, 0, 1);

    }

    .grila_1_interior_grupa_2:hover .info_container_imag_3 {
      opacity: 1;
      transform: translate(-50%, -16px);
    }
  

  /* Grila 2 */

  .grila_2_cont{

    display: flex;
    flex-direction: column;
    gap: 24px;

    width: 488px;
    height: 804px;
  }

  .grila_2{

    border-radius: 48px;
    flex-shrink: 0;

    width: 488px;
    height: 804px;
  
    overflow: hidden; 
    position: relative; 

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .grila_2::before{

    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/paris.jpg) rgb(255, 255, 255) 50% / cover no-repeat;

    background-size: 100%; 
    transition: all 800ms cubic-bezier(0.3, 0, 0, 1); 

  }

  .grila_2:hover::before{
    background-size: 108%; /* Zoom the background further on hover */
    /* opacity: 0.72; */
  }

  .info_container{
    position: absolute;
    bottom: 12px;
    left: 50%;
    transform: translate(-50%, 0);

    display: flex;
    width: 228px;
    padding: 23px 16px;
    justify-content: space-between;
    align-items: baseline;

    border-radius: 32px;
    /* border: 1px solid rgba(255, 255, 255, 0.24); */
    background: rgba(104, 97, 155, 0.08);
    backdrop-filter: blur(16px);


    opacity: 1;
    transition: all 800ms cubic-bezier(0.3, 0, 0, 1);

  }

  .grila_2:hover .info_container {
    opacity: 1;
    transform: translate(-50%, -16px);
  }

    .info_title{
      color: #FFF;
      text-align: center;
      font-family: Jost;
      font-size: 24px;
      font-style: normal;
      font-weight: 400;
      line-height: 32px; /* 133.333% */
    }

    .price_container{
      display: flex;
      justify-content: flex-end;
      align-items: baseline;
      gap: 8px;
    }

    .price_text{
      color: #FFF;
      text-align: center;
      font-family: Jost;
      font-size: 24px;
      font-style: normal;
      font-weight: 400;
      line-height: 32px; /* 133.333% */
    }

    .from_text{
      color: rgba(255, 255, 255, 0.48);
      text-align: center;
      font-family: Jost;
      font-size: 14px;
      font-style: normal;
      font-weight: 400;
      line-height: normal;
    }



  /* grila trei */

  .grila_3{

    display: flex;
    flex-direction: column;
    gap: 40px;

    width: 488px;
    height: 804px;
  }

  .grila_3_interior_1{
    border-radius: 48px;
    flex-shrink: 0;

    width: 488px;
    height: 382px;

  
    overflow: hidden; 
    position: relative; 

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .grila_3_interior_1::before{

    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/greece.jpg) rgb(255, 255, 255) 50% / cover no-repeat;

    background-size: 100%; 
    transition: all 800ms cubic-bezier(0.3, 0, 0, 1); 

  }

  .grila_3_interior_1:hover::before{
    background-size: 108%; 
  }

    .info_container_imag_5{
      position: absolute;
      bottom: 12px;
      left: 50%;
      transform: translate(-50%, 0);

      display: flex;
      width: 228px;
      padding: 23px 16px;
      justify-content: space-between;
      align-items: baseline;

      border-radius: 32px;
      /* border: 1px solid rgba(255, 255, 255, 0.24); */
      background: rgba(104, 97, 155, 0.08);
      backdrop-filter: blur(16px);


      opacity: 1;
      transition: all 800ms cubic-bezier(0.3, 0, 0, 1);

    }

    .grila_3_interior_1:hover .info_container_imag_5 {
      opacity: 1;
      transform: translate(-50%, -16px);
    }

  .grila_3_interior_2{
    border-radius: 48px;
    flex-shrink: 0;

    width: 488px;
    height: 382px;

  
    overflow: hidden; 
    position: relative; 

    cursor: pointer;
    transition: all 400ms cubic-bezier(0.3, 0, 0, 1);
  }

  .grila_3_interior_2::before{

    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: inherit;

    background: url(/src/components/media/carpati.jpg) rgb(255, 255, 255) 50% / cover no-repeat;

    background-size: 100%; 
    transition: all 800ms cubic-bezier(0.3, 0, 0, 1); 

  }

  .grila_3_interior_2:hover::before{
    background-size: 108%; 
  }

  .info_container_imag_6{
      position: absolute;
      bottom: 12px;
      left: 50%;
      transform: translate(-50%, 0);

      display: flex;
      width: 228px;
      padding: 23px 16px;
      justify-content: space-between;
      align-items: baseline;

      border-radius: 32px;
      /* border: 1px solid rgba(255, 255, 255, 0.24); */
      background: rgba(104, 97, 155, 0.08);
      backdrop-filter: blur(16px);


      opacity: 1;
      transition: all 800ms cubic-bezier(0.3, 0, 0, 1);

    }

    .grila_3_interior_2:hover .info_container_imag_6 {
      opacity: 1;
      transform: translate(-50%, -16px);
    }


</style>