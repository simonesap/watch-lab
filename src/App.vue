<template>

  <div>

    <HomePage/>

  </div>

</template>

<script>
import HomePage from "./components/pages/HomePage.vue";

export default {
  name: 'App',
  components: {
    HomePage,
  }
}
</script>

<style lang="scss">
@import './assets/style/sass/app.scss';

</style>
