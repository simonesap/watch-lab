<template>
  <div class="">
    <VueSlickCarousel class="" :arrows="true" :dots="true">

        <div class="d_flex flex_column">
            <div></div>

            <div class="mt-48 d_flex flex_between flex_column">
                
                <div class="w_5"></div>
                
                <div class="w_15 ">
                    <h2 class="text_uppercase">watch/lab</h2>
                </div>
                
                <div class="w_80 mt-48">
                    <img class="w_100 h_100" src="../../assets/img/kisspng-imac-macbook-pro-graphics-cards-video-adapters-mac-5abc4645d4b808.8436230515222881978713.png" alt="Macchintosh Maschine">
                </div>
            
            </div>
            
        </div>

        <div>
            <img class="w_100 h_100" src="../../assets/img/gabriel-beaudry-ntX2TjKrzLc-unsplash.jpg" alt="Macchintosh Maschine">
        </div>

    </VueSlickCarousel>
  </div>
</template>
 
<script>
  import VueSlickCarousel from 'vue-slick-carousel'
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  // optional style for arrows & dots
//   import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
 
  export default {
    name: 'VueSlickComp',
    components: { VueSlickCarousel },
  }
</script> 

<style lang="scss">
@import "../../assets/style/sass/app.scss";


</style>