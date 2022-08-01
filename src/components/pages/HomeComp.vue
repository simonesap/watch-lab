<template>

  <div>

    <HeaderComp/>

    <!--Jumbo-->
    <SliderComp/>

    <main class="container_main">
      <div class="vh_100 w_100 d_flex flex_wrap">
        <div class="w_50">
          <h2 class="mt-56 fs_4 w_80">History and Patriarcal season</h2>
        </div>
        <div class="w_100 d_flex">
          <div class="w_50">
            <p class="mt-8 gray fs_1_02 mb-56 w_80">
              On the other hand, we denounce with righteous
              indignation and dislike men who are so beguiled and
              demoralized by the charms of pleasure of the moment,
              so blinded by desire
            </p>
          </div>
          
          <div class="w_50">
            <p class="mt-8 gray fs_1_02 mb-40 w_80">
              But I must explain to you how all this mistaken idea of denouncing
              pleasure and praising pain was born and I will give you a complete
              account of the system, and expound the actual teachings of the great
              explorer of the truth, the master-builder of human happiness. No that
              are extremely painful
            </p>
          </div>
          
        </div>
      </div>

      <div class="w_100 d_flex align_center">
        <div class="w_50">
      <div class="text_center mb-40"> 
              <h4 class="mt-40 text_uppercase text_center">london collection season</h4>
              <h2 class="fs_3 text_center mt-32">Temporary Store</h2>
              <p class="mlr_auto gray fs_1_02 mt-72 w_75">On the other hand, we denounce with righteous
                                                          indignation and dislike men who are so beguiled and
                                                          demoralized by the charms of pleasure of the moment,
                                                          so blinded by desire
              </p>
              <button class="text_capital mb-56 text_center mlr_auto mt-72 pt-16 pb-16 pl-64 pr-64 btn_gold fs_1_02 gold">View</button>
          </div>
        </div>
        <div class="w_50">
          <img class="w_100 h_100" src="../../assets/img/1.png" alt="">
        </div>
      </div>

      <div class="w_100 d_flex align_center">
        <div class="w_50">
          <img class="w_100 h_100 mb-56" src="../../assets/img/2.png" alt="">
        </div>
        <div class="w_50">
          <div class="text_center mb-56"> 
              <!-- v-if="indexImg == 0" -->
              <h4 class="mt-56 text_uppercase text_center">london collection season</h4>
              <h2 class="fs_3 text_center mt-32">New Collection Henry London</h2>
              <p class="mlr_auto gray fs_1_02 mt-72 w_75">On the other hand, we denounce with righteous
                                                          indignation and dislike men who are so beguiled and
                                                          demoralized by the charms of pleasure of the moment,
                                                          so blinded by desire
              </p>
              <button class="text_capital mb-56 text_center mlr_auto mt-72 pt-16 pb-16 pl-64 pr-64 btn_gold fs_1_02 gold">View</button>
          </div>
        </div>
      </div>

      <div class="w_100 vh_95 d_flex mt-56 mb-56 p_relative">
        <div class="w_50 t_0">
            <h2 class="p-0 fs_4 w_85">Press from</h2>
            <h2 class="p-0 fs_4 w_80">Watch Lab Studio</h2>
            <p class="mt-72 gray fs_1_02 mb-56 w_50 p-0">
              On the other hand, we denounce with
              righteous indignation and dislike men
              who are so beguiled and demoralized
              by the charms of pleasure of the
              moment, so blinded by desire, that
              they cannot foresee the pain trouble
            </p>
        </div>
       
        <img class="w_100 h_400 p_absolute w_600px main_slider" :src="sliderImg[indexImg].url" alt="index">
     
        <div class="w_50 ml-80 h_100 bg_light_gray">
          <div class="d_flex flex_between">
            <div class="w_50"></div>
            <div class="w_50">
              <h4 class="mt-190 text_uppercase">PRESS</h4>
              <h4 class="text_uppercase gold">18 SETTEMBRE 2015</h4>
            </div>
          </div>
          <div class="d_flex">
            <div class="w_50"></div>
            <h2 class="fs_2 mt-32 w_40">Most Important Days on Watchlab</h2>
          </div>
          <div class="d_flex">
            <div class="w_50"></div>
            <div class="w_50 d_flex ml-24">
              <div @click="prev()" role="button" class="mt-32 pointer"><i class="fa-solid fa-angle-left mr-8"></i></div>
              <div @click="next()" class="mt-32 ml-40 pointer"><i class="fa-solid fa-angle-right ml-8"></i></div>
            </div>
          </div>
            
        </div>
        
      </div>

      <div class="vh_80 mt-100 mb-56 d_flex">
        <div class="w_50 h_100 pointer">
          <img class="w_100 h_100" src="../../assets/img/1-f.png" alt="">
        </div>
        <div class="w_50 h_100 d_flex flex_wrap">
            <div class="w_2 h_50">
              <img class="w_100 h_100" src="../../assets/img/2-f.png" alt="">
            </div>
            <div class="w_2 h_50">
              <img class="w_100 h_100" src="../../assets/img/3-f.png" alt="">
            </div>
            <div class="w_2 h_50">
              <img class="w_100 h_100" src="../../assets/img/5-f.png" alt="">
            </div>
            <div class="w_2 h_50">
              <img class="w_100 h_100" src="../../assets/img/4-f.png" alt="">
            </div>  
        </div>
      </div>

    </main>

    <footer class="container_main d_flex flex_column mb-56">
      <div class="h_30 bg_footer">
        <div class="text_center mb-56 text_white"> 
            <h2 class="fs_3 text_center mt-32">Get in Touch</h2>
            <h4 class="mt-56 text_uppercase text_center">DISCOVER MORE ABOUT NEWS, EXCLUSIVE EVENTS AND DISCOUNT</h4>
            <div>
              <button class="text_center mlr_auto mt-72 pt-16 pb-16 pl-64 pr-64 btn_gold fs_1_02" placeholder="type your email"></button>
              <button class="mb-56 pt-16 pb-16 pl-64 pr-64 btn_gold fs_1_02">ok</button>
            </div>
        </div>
      </div>
      <div class="h_60 bg_black_footer">
        <div><h2>WATCH/LAB</h2></div>
        <div>
          <ul>
            <li></li>
            <li></li>
            <li></li>
          </ul>
        </div>
      </div>
    </footer>

  </div>

</template>

<script>
import HeaderComp from "../HeaderComp.vue";
import SliderComp from "../includes/SliderComp.vue";

export default {
  name: 'HomeComp',
  components: {
    HeaderComp,
    SliderComp
  },
  data(){
        return {
            indexImg: 0,
            timer: null,
            sliderImg: [
                { url: require("../../assets/img/3.png") },
                { url: require("../../assets/img/henry-HQ-1.png") },
                { url: require("../../assets/img/henry-about-caseback-680x526px.webp") },
                
            ],
        }
    },
    methods: {
        next: function() {
            this.indexImg++
            if (this.indexImg == this.sliderImg.length) {
                this.indexImg = 0    
            } 
        },
        prev: function() {
            this.indexImg--
            if (this.indexImg == -1) {
                this.indexImg = this.sliderImg.length -1
            }
        },
        startSlide: function() {
        this.timer = setInterval(this.next, 8000);
        }
    },
    mounted: function() {
        this.startSlide();
  }
}
</script>

<style lang="scss">
@import '../../assets/style/sass/app.scss';

  .bg_footer{
    background-image: url('../../assets/img/scott-webb-p-0lWFknspg-unsplash.jpg');
    background-position: center;
    background-size: cover;
    filter: opacity(0.8);
}
// filter: sepia(50%);

</style>
