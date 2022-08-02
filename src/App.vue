<template>

  <div>

    <HomeComp/>

  </div>

</template>

<script>
import HomeComp from "./components/pages/HomeComp.vue";

export default {
  name: 'App',
  components: {
    HomeComp,
  }
}
</script>

<style lang="scss">
@import './assets/style/sass/app.scss';

body{
  font-family: 'Merriweather-Regular', serif;
}

</style>
