<template>
    <div>
        <div>
            <div>
                <div class="w_100">    

                    <!--Carousel-->
                    <div class="myCarousel-box">
                        
                        <div class="myCarousel-item" :class="(indexImg == 1) ? 'henry_london_black' : '' ">

                            <!--Watch-img-->
                            <div v-if="indexImg == 1">
                                <div>
                                    <h4 @click="prev()" :class="(indexImg != 3) ? 'text_white' : '' " role="button" class="ml-24 opa_06_hov arrow-lft text_uppercase montserrat-bold"><i class="fa-solid fa-angle-left mr-8"></i>Previous</h4>
                                </div>
                                <img :class="(indexImg == 1) ? 'opa_05' : '' "   class="w_100" :src="backgroundImage[indexImg].url" alt="index">
                                <div v-if="indexImg != 3" @click="next()" class="next_container bg_white">
                                    <img class="w_100 p_relative" :src="backgroundImage[indexImg + 1].url" alt="index">
                                    <h4 v-if="indexImg == 1" :class="(indexImg == 0) ? 'text_white' : '' " role="button" class="text_uppercase text_hover p_absolute mt-170 ml-230 montserrat">Next <i class="fa-solid fa-angle-right ml-8 mr-8"></i> </h4>
                                </div>
                                <div v-if="indexImg == 1" class="jumbo_text text_white d_flex flex_wrap">
                                    <h2 class="text_white fs_3 mt-8 w_75">The Path to Success with Watchlab</h2>
                                </div>
                            </div>

                            <!--Apple-img-->
                            <div v-if="indexImg == 3" class="d_flex flex_column">

                                <div class="mt-48 d_flex flex_between flex_column">
                                    <div v-if="indexImg != 0" class="">
                                        <h4 @click="prev()" :class="(indexImg != 2 & indexImg != 3) ? 'text_white' : '' " role="button" class="ml-24 opa_06_hov arrow-lft text_uppercase montserrat-bold"><i class="fa-solid fa-angle-left mr-8"></i> Previous</h4>
                                    </div>
                                    <div class="w_15 ml-100">
                                        <h2 class="text_uppercase fs_2 montserrat-bold">watch/lab</h2>
                                    </div>
                                    <div class="bg_apple_desk"></div>
                                </div>
                                
                            </div>

                            <!-- != from img-1 -->
                            <div v-if="indexImg != 1" class="p_relative d_flex flex_center">
                                <div v-if="indexImg != 0 & indexImg != 3" class="">
                                    <h4 @click="prev()" :class="(indexImg != 3) ? 'text_white' : '' " role="button" class="ml-24 opa_06_hov arrow-lft text_uppercase montserrat-bold"><i class="fa-solid fa-angle-left mr-8"></i>Previous</h4>
                                </div>
                                <img  class="w_100" :src="backgroundImage[indexImg].url" :class="(indexImg == 0) ? 'opa' : '' " alt="index">
                                <div v-if="indexImg == 0" class="jumbo_text text_white d_flex flex_wrap"> 
                                    <span class="text_uppercase text_center montserrat-bold">london collection season</span>
                                    <h2 class="text_center mt-56 fs_4">New Selection Of Herny London</h2>
                                    <p class="text_center mt-24 w_100 montserrat-bold">An estimable experience in the modern collection house</p>
                                    <button class="text_capital text_center mt-72 pt-8 pb-8 pl-72 pr-72 btn fs_1_02 text_white merriweather-regular">discover</button>
                                </div>
                                <div v-if="indexImg != 3" @click="next()" class="next_container bg_white d_none_1248">
                                    <img class="w_100 p_relative" :src="backgroundImage[indexImg + 1].url" alt="index">
                                    <div v-if="indexImg == 0" class="jumbo_text_2 text_white d_flex flex_wrap">
                                        <h3 class="text_white w_40 ml-neg">The Path to Success with Watchlab</h3>
                                    </div>
                                    <h4 v-if="indexImg == 0" :class="(indexImg == 0) ? 'text_white' : '' " role="button" class="text_uppercase text_hover p_absolute mt-200 ml-200 montserrat-bold">Next <i class="fa-solid fa-angle-right ml-8 mr-8"></i> </h4>
                                    <h4 v-if="indexImg == 1" :class="(indexImg == 0) ? 'text_white' : '' " role="button" class="text_uppercase text_hover p_absolute mt-170 ml-230 montserrat-bold">Next <i class="fa-solid fa-angle-right ml-8 mr-8"></i> </h4>
                                    <h4 v-if="indexImg != 0 & indexImg != 1" :class="(indexImg == 0) ? 'text_white' : '' " role="button" class="text_uppercase text_hover p_absolute mt-220 ml-200 montserrat-bold">Next <i class="fa-solid fa-angle-right ml-8 mr-8"></i> </h4>
                                </div>
                            </div>
                            
                        </div>
                        
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    
    name: "SliderComp",
    data(){
        return {
            indexImg: 0,
            timer: null,
            backgroundImage: [
                { url: require("../../assets/img/damir-kopezhanov-VM1Voswbs0A-unsplash.jpg") },
                { url: require("../../assets/img/Henry-London (1).webp") },
                { url: require("../../assets/img/Untitled (5).png") },
                { url: require("../../assets/img/3D Transformer (Community) .png") },
            ],
        }
    },
    methods: {
        next: function() {
            this.indexImg++
            if (this.indexImg == this.backgroundImage.length) {
                this.indexImg = 0    
            } 
        },
        prev: function() {
            this.indexImg--
            if (this.indexImg == -1) {
                this.indexImg = this.backgroundImage.length -1
            }
        },
        startSlide: function() {
        this.timer = setInterval(this.next, 10000);
        }
    },
//     mounted: function() {
//         this.startSlide();
//   }
}
</script>

<style lang="scss">

        // .myCarousel-box {
        //     width: 100%;
        //     display: flex;
        //     // flex-direction: column;
        //     flex-wrap: wrap;
        // }

        .myCarousel-box .myCarousel-item {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .myCarousel-box {  
            // margin: 24px 0;
            // height: 90vh;
            display: flex;
            justify-content: space-between;
            flex-wrap: nowrap;
            position: relative;
            width: 100%;
            
            .myCarousel-item {
                display: flex;
                justify-content: center;
                width: 100%;
                align-items: center;

                
                &.myCarousel-item:active {
                    background-color: darken($color: #f1f4f9, $amount: 1);
                }
                // img {
                //     width: 100%;
                //     position: relative;

                // }
            }

            // img {
            //         width: 100%;
            //         position: relative;

            //     }

            .arrow-lft {
                height: 40px;
                width: 40px;
                display: flex;
                align-items: center;
                justify-content: center;
                position: absolute;
                top: 95%;
                left: 24px;
                transform: translate(0,-50%);
                padding: 4px 4px;
                &:hover {
                    color: rgba(245, 18, 18, 0.925);
                    cursor: pointer;
                }
            }
            .arrow-rgt {
                height: 40px;
                width: 40px;
                display: flex;
                align-items: center;
                justify-content: center;
                position: absolute;
                top: 95%;
                right: 10px;
                transform: translate(-50%,-50%);
                padding: 4px 4px;
                &:hover {
                    color: rgba(245, 18, 18, 0.925);
                    cursor: pointer;
                }
            }
            
        }

        .jumbo_text{
            width: 600px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: absolute;
            top: 20%;
            padding: 4px 4px;
        }

        .jumbo_text_2{
            width: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: absolute;
            top: 10%;
            padding: 4px 4px;
        }

        .next_container{
            width: 300px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: absolute;
            top: 83%;
            right: -100px;
            transform: translate(-50%,-50%);
            padding: 4px 4px;
            &:hover {
                cursor: pointer;
            }
            &:hover {
                opacity: 0.6;
            }
        }

        .text_hover:hover {
            color: rgba(245, 18, 18, 0.925);    
        }

        .opa{
            opacity: 0.9;
            // filter: contrast(200%);
            // filter: saturate(800%);
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