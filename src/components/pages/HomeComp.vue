<template>

  <div>

    <HeaderComp/>

    <!--Jumbo-->
    <SliderComp/>

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
  }
}
</script>

<style lang="scss">
@import '../../assets/style/sass/app.scss';

</style>
