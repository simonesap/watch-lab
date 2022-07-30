<template>

  <div>

    <HeaderComp/>

    <!--Jumbo-->
    <div>
      <!-- <VueSlickComp/> -->
    </div>

    <!-- <SliderComp/> -->

    <SliderCompDue/>

  </div>

</template>

<script>
import HeaderComp from "../HeaderComp.vue";
// import VueSlickComp from "./../includes/VueSlickComp.vue";
// import SliderComp from "../includes/SliderComp.vue";
import SliderCompDue from "../includes/SliderCompDue.vue";

export default {
  name: 'HomePage',
  components: {
    HeaderComp,
    // VueSlickComp,
    // SliderComp,
    SliderCompDue
  }
}
</script>

<style lang="scss">
@import '../../assets/style/sass/app.scss';

</style>
