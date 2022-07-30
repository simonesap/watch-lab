<!--<template>

  <div>

    <div class="" :class="classContainer">
        <div class="h_100 d_flex flex_center align_center">
            <div class="text_center d_flex flex_between">
                <button class="border-0">
                    <i @click="nextPhotoLeft" class="fa-solid fa-angle-left"></i>
                </button>
                <img :src="mediaImg[counterImg]" class="img-fluid rounded" v-bind:class="classiImg">
                <button class="border-0" @click="nextPhotoRight">
                    <i class="fa-solid fa-angle-right"></i>
                </button>
            </div>
        </div>
    </div>

  </div>
</template>
 
<script>
 
  export default {
    name: 'SliderComp',

    data() {
            return {
                mediaImg: [require'../../assets/img/kisspng-imac-macbook-pro-graphics-cards-video-adapters-mac-5abc4645d4b808.8436230515222881978713.png'
                        ],
                        classiImg: 'middle',
                        classContainer: 'h_100',
                        counterImg: 0,
                        }
        },

        
        // created() {
        //     this.nextPhotoTiming();
        // },

        methods: {

            // Funzione per spostarsi di un elemento a destra nell''array
            nextPhotoRight: function(){
                this.counterImg += 1;
                if(this.counterImg > (this.mediaImg.length -1)){
                    this.counterImg = 0;
                }
            },

            // Funzione per spostarsi di un elemento a sinistra nell''array
            nextPhotoLeft: function(){
                this.counterImg -= 1;
                if(this.counterImg < 0){
                    this.counterImg = this.mediaImg.length - 1;
                }
            },

            // Funzione per l'intervallo di tempo
            // nextPhotoTiming: function(){
            //     setInterval(() => {
            //         this.nextPhotoRight();
            //     },3000);
            // },

            // Funzione per vedere la foto cliccata secondo l'indice comune di foto e pallino
            clickDots: function(indexPhoto){
                console.log(indexPhoto);
                    this.counterImg = indexPhoto;
            }
    
        }
    
  }
</script> 

<style lang="scss">
@import "../../assets/style/sass/app.scss";


</style>-->
      
      
