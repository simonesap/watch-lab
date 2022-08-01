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

// @font-face {
//   font-family: 'Merriweather-Regular';
//   src: url('C:\Users\matte\OneDrive\Desktop\Projects\VsCode\Freelance\watch-lab\src\assets\fonts\Merriweather-Regular.ttf');
// }

@font-face {
  font-family: 'Montserrat-Bold';
  src: url('C:\Users\matte\OneDrive\Desktop\Projects\VsCode\Freelance\watch-lab\src\assets\fonts\Montserrat-Bold.ttf');
}

  

</style>
