<template>
    <div>
        <div>
            <div>
                <div class="w_100">    
                    <div class="myCarousel-box">
                        
                        <div class="myCarousel-item">

                            <div v-if="indexImg == 2" class="d_flex flex_column">

                                <div class="mt-48 d_flex flex_between flex_column">
                                    <div v-if="indexImg != 0" class="">
                                        <h4 @click="prev()" :class="(indexImg != 1 & indexImg != 2) ? 'text_white' : '' " role="button" class="ml-24 arrow-lft text_uppercase"><i class="fa-solid fa-angle-left mr-8"></i> Previous</h4>
                                    </div>
                                    <div class="w_15 ml-100">
                                        <h2 class="text_uppercase">watch/lab</h2>
                                    </div>
                                    <div class="bg_apple_desk"></div>
                                    <div class="">
                                        <h4  @click="next()" :class="(indexImg != 1 & indexImg != 2) ? 'text_white' : '' " role="button" class="arrow-rgt text_uppercase">Next <i class="fa-solid fa-angle-right ml-8"></i></h4>
                                    </div>
                                </div>
                                
                            </div>

                            <div class="p_relative">
                                <div v-if="indexImg != 0 & indexImg != 2" class="">
                                    <h4 @click="prev()" :class="(indexImg != 2) ? 'text_white' : '' " role="button" class="ml-24 arrow-lft text_uppercase"><i class="fa-solid fa-angle-left mr-8"></i>Previous</h4>
                                </div>
                                <img class="w_100" :src="backgroundImage[indexImg].url" alt="index">
                                <div class="jumbo_text"> 
                                    <!-- v-if="indexImg == 0" -->
                                    <h4 class="text_uppercase text_center">london collection season</h4>
                                    <h2 class="text_center">New Selection Of Herny London</h2>
                                    <div></div>
                                    <div></div>
                                </div>
                                <div v-if="indexImg != 2" class="">
                                    <h4 @click="next()" :class="(indexImg != 2) ? 'text_white' : '' " role="button" class="arrow-rgt text_uppercase">Next <i class="fa-solid fa-angle-right ml-8"></i></h4>
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
                { url: require("../../assets/img/nastuh-abootalebi-J1rNS2qv8BQ-unsplash.jpg") },
                { url: require("../../assets/img/gabriel-beaudry-ntX2TjKrzLc-unsplash.jpg") },
                { url: require("../../assets/img/kisspng-imac-macbook-pro-graphics-cards-video-adapters-mac-5abc4645d4b808.8436230515222881978713.png") },
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
        this.timer = setInterval(this.next, 8000);
        }
    },
    mounted: function() {
        this.startSlide();
  }
}
</script>

<style lang="scss" scoped>

        .myCarousel-box[data-v-1f1efff0] {
            display: flex;
            // flex-direction: column;
            flex-wrap: wrap;
        }

        .myCarousel-box .myCarousel-item[data-v-1f1efff0] {
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
            display: flex;
            align-items: center;
            justify-content: center;
            position: absolute;
            top: 50%;
            transform: translate(-50%,-50%);
            padding: 4px 4px;
        }

</style>