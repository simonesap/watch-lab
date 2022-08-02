<template>

  <div>

    <HeaderComp/>

    <!--Jumbo-->
    <SliderComp/>

    <main class="container_main">
      <div class="vh_70 w_100 d_flex flex_wrap">
        <div class="w_50">
          <h2 class="mt-56 mb-24 fs_4 w_80">History and Patriarcal season</h2>
        </div>
        <div class="w_100 d_flex mb-56">
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
              <h4 class="mt-40 text_uppercase text_center montserrat-bold">london collection season</h4>
              <h2 class="fs_3 text_center mt-32">Temporary Store</h2>
              <p class="mlr_auto gray fs_1_02 mt-72 w_60">On the other hand, we denounce with righteous
                                                          indignation and dislike men who are so beguiled and
                                                          demoralized by the charms of pleasure of the moment,
                                                          so blinded by desire
              </p>
              <button class="text_capital mb-56 text_center mlr_auto mt-72 pt-8 pb-8 pl-72 pr-72 btn_gold fs_1_02 gold">View</button>
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
              <h4 class="mt-56 text_uppercase text_center montserrat-bold">london collection season</h4>
              <h2 class="fs_3 mlr_auto text_center mt-32 w_50">New Collection Henry London</h2>
              <p class="mlr_auto gray fs_1_02 mt-72 w_60">On the other hand, we denounce with righteous
                                                          indignation and dislike men who are so beguiled and
                                                          demoralized by the charms of pleasure of the moment,
                                                          so blinded by desire
              </p>
              <button class="text_capital mb-56 text_center mlr_auto mt-72 pt-8 pb-8 pl-72 pr-72 btn_gold fs_1_02 gold">View</button>
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
              <h4 class="mt-190 text_uppercase montserrat-bold">PRESS</h4>
              <h4 class="text_uppercase gold montserrat-bold">18 SETTEMBRE 2015</h4>
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

    <footer class="container_main d_flex flex_column mb-56 vh_130">
      <div class="h_40 bg_footer p_relative">
        <div class="bg_orange p_absolute w_100 h_100 d_flex flex_center">
          <div class="text_center mb-56 text_white w_350px"> 
            <h2 class="fs_3 text_center mt-32">Get in Touch</h2>
            <span class="mt-24 text_uppercase text_center montserrat-bold">DISCOVER MORE ABOUT NEWS, EXCLUSIVE EVENTS AND DISCOUNT</span>
            <div class="d_flex">
              <input type="text" class="text_white mlr_auto mt-40 pt-16 pb-16 pl-24 pr-24 btn_gold fs_1_02" placeholder="type your email">
              <button type="submit" class="text_white ml-16 mt-40 pt-16 pb-16 pl-24 pr-24 btn_gold fs_1_02">ok</button>
            </div>
          </div>
        </div>
      </div>
      <div class="h_60 bg_black_footer text_white d_flex flex_center flex_wrap align_center">
        <div class="">
          <div class="w_100 mb-40">
            <h2 class="fs_2 montserrat-bold">WATCH/LAB</h2>
          </div>
          <ul class="d_flex">
            <li class="w_280px w_200px_950 w_100px_769 w_200px_806 d_flex flex_wrap mr-72">
              <a class="mt-16 decoration_none w_100" href="#">Watch/Lab Innovation brings success</a>
              <a class="mt-16 decoration_none w_100" href="#">Via Borgogna 5, Milan</a>
              <a class="mt-16 decoration_none w_100" href="#">Italy</a>
            </li>
            <li class="w_200px w_200px_950 w_100px_769 w_200px_806 d_flex flex_wrap">
              <a class="mt-16 decoration_none w_100" href="#">About us</a>
              <a class="mt-16 decoration_none w_100" href="#">Brand</a>
              <a class="mt-16 decoration_none w_100" href="#">Projects</a>
              <a class="mt-16 decoration_none w_100" href="#">Magazine</a>
            </li>
            <li class="w_200px w_200px_950 w_100px_769 w_200px_806 d_flex flex_wrap">
              <a class="mt-16 decoration_none w_100" href="#">Press</a>
              <a class="mt-16 decoration_none w_100" href="#">Contacts</a>
              <a class="mt-16 decoration_none w_100" href="#">Privacy Polocy</a>
              <a class="mt-16 decoration_none w_100" href="#">Search</a>
            </li>
            <li class="w_200px w_200px_950 w_100px_769 w_150px_806 d_flex flex_wrap">
              <a class="mt-16 decoration_none w_100" href="#">T. +39 392 9133937</a>
              <a class="mt-16 decoration_none w_100" href="#">M. info@watch-lab.it</a>
              <a class="mt-16 decoration_none w_100 montserrat-bold" href="#">FACEBOOK</a>
              <a class="mt-16 decoration_none w_100 montserrat-bold" href="#">INSTAGRAM</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="vh_10 bg_black_footer_2 d_flex align_center mb-56">
        <div class="container_footer d_flex flex_between align_center">
          <span class="gold">Copyright Watch/Lab all rights reserved</span>
          <span class="gold">website by nssfactory</span>
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

<style lang="scss" scoped>
@import '../../assets/style/sass/app.scss';

  .bg_footer{
    background-image: url('../../assets/img/scott-webb-p-0lWFknspg-unsplash.jpg');
    background-position: center;
    background-size: cover;
    filter: opacity(0.6);
}

  .bg_orange{
    background-color: rgba(255, 166, 0, 0.129);
  }
  // filter: sepia(50%);

  .bg_black_footer{
    background-color: #333333;
  }

  .bg_black_footer_2{
    background-color: #303030;
  }

  input::placeholder {
    color: white;
    text-align: start;
    margin-left: 0;
  }

  .t_50{
    top: 50%;
  }

  .left_50{
    left: 50%;
  }

  footer{
    span{
      color: #e5ded6;
    }
    a{
      color: #e5ded6;
    }
    a:hover{
      cursor: pointer;
       color: #a7a8b1;
    }
  }

  input:hover{
      cursor: pointer;
       color: #a7a8b1;
    }

  button:hover{
    cursor: pointer;
      color: #a7a8b1;
  }

  // Font
        .montserrat-bold {
            font-family: 'Montserrat-Bold', sans-serif;
        }

        // Font
        .montserrat {
            font-family: 'Montserrat-Regular', sans-serif;
        }

        .merriweather-regular{
            font-family: 'Merriweather-Regular', serif;
        }

</style>
