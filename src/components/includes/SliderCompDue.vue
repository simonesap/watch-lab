<template>
    <div>
        <div>
            <div>
                <div class="w_100">    
                        <div class="myCarousel-box">
                            <div class="arrow-lft" @click="prev()">
                                <i class="fas fa-arrow-left"></i>
                            </div>
                            <div class="myCarousel-item" @click="prev()">
                                <img class="w_100" :src="logoArr[indexImg].url" alt="index" >
                            </div>
                            <!-- <div class="myCarousel-item" >
                                <img class="w_100" :src="logoArr2[indexImg].url" alt="index" >
                            </div>
                            <div class="myCarousel-item" @click="next()" >
                                <img class="w_100" :src="logoArr3[indexImg].url" alt="index" >
                            </div> -->
                            <div class="arrow-rgt" @click="next()">
                                <i class="fas fa-arrow-right"></i>
                            </div>
                        </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    
    name: "SliderCompDue",
    data(){
        return {
            indexImg: 0,
            timer: null,
            logoArr: [
                { url: require("../../assets/img/kisspng-imac-macbook-pro-graphics-cards-video-adapters-mac-5abc4645d4b808.8436230515222881978713.png") }, //1
                { url: require("../../assets/img/gabriel-beaudry-ntX2TjKrzLc-unsplash.jpg") },
            ],
            // logoArr2: [
            //     { url: require("../../assets/img/gabriel-beaudry-ntX2TjKrzLc-unsplash.jpg") },
            //     { url: require("../../assets/img/gabriel-beaudry-ntX2TjKrzLc-unsplash.jpg") },
            // ],
            // logoArr3: [
            //     { url: require("../../assets/img/gabriel-beaudry-ntX2TjKrzLc-unsplash.jpg") },
            //     { url: require("../../assets/img/gabriel-beaudry-ntX2TjKrzLc-unsplash.jpg") },
            // ]
        }
    },
    methods: {
        next: function() {
            this.indexImg++
            if (this.indexImg == this.logoArr.length) {
                this.indexImg = 0    
            }
        },
        prev: function() {
            this.indexImg--
            if (this.indexImg == -1) {
                this.indexImg = this.logoArr.length -1
            }
        },
        startSlide: function() {
        this.timer = setInterval(this.next, 4000);
        }
    },
    mounted: function() {
        this.startSlide();
  }
}
</script>

<style lang="scss" scoped>

        .myCarousel-box[data-v-1f1efff0] {
            margin: 24px 0;
            height:100vh;
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            position: relative;
        }

        .myCarousel-box .myCarousel-item[data-v-1f1efff0] {
            display: flex;
            justify-content: center;
            width: 100vh;
            align-items: center;
            border-radius: 5px;
        }

        .myCarousel-box {  
            margin: 24px 0;
            height: 150px;
            display: flex;
            justify-content: space-between;
            flex-wrap: nowrap;
            position: relative;
            .arrow-lft {
                height: 40px;
                width: 40px;
                display: flex;
                align-items: center;
                justify-content: center;
                position: absolute;
                top: 50%;
                left: 0;
                transform: translate(0,-50%);
                border: 1px solid #242424;
                border-radius: 50%;
                padding: 4px 4px;
                &:hover {
                    background-color: rgba(0, 0, 0, 0.1);
                }
                i {
                    color: #242424;
                }
            }
            .arrow-rgt {
                height: 40px;
                width: 40px;
                display: flex;
                align-items: center;
                justify-content: center;
                position: absolute;
                top: 50%;
                right: 0;
                transform: translate(-50%,-50%);
                border: 1px solid #242424;
                border-radius: 50%;
                padding: 4px 4px;
                &:hover {
                    background-color: rgba(0, 0, 0, 0.1);
                }
                i {
                    color: #242424;
                }
            }
            .myCarousel-item {
                display: flex;
                justify-content: center;
                width: calc(100% / 3 - 4px);
                align-items: center;
                // border: 1px solid rgba(36, 36, 36, 0.1);
                border-radius: 5px;
                
                &.myCarousel-item:active {
                    background-color: darken($color: #f1f4f9, $amount: 1);
                }
                img {
                    width: 100%;
                }
            }
            
        }

</style>