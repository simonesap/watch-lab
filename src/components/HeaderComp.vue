<template>

  <div class="w_100 bg_white">

    <nav class="w_100">
      <ul class="d_flex flex_between m_0">
        <li class="w_80 d_flex flex_between align_center m_0 montserrat-bold ">
          <a href="#" class="bg_beige p-16 m_0 text_uppercase mt-32 ml-32 d_flex align_center">
             <h3 class="text_white fs_1_08">watch/lab</h3>
          </a>
          <a href="#" class="p-16 d_flex align_center">
             <h5 class="fs_1">About us</h5>
          </a>
          <a href="#" class="p-16 d_flex align_center">
             <h5 class="fs_1">Brand</h5>
          </a>
          <a href="#" class="p-16 d_flex align_center">
             <h5 class="fs_1">Projects</h5>
          </a>
          <a href="#" class="p-16 d_flex align_center">
             <h5 class="fs_1">Magazine</h5>
          </a>
          <a href="#" class="p-16 d_flex align_center">
             <h5 class="fs_1">Press</h5>
          </a>
          <a href="#" class="p-16 d_flex align_center">
             <h5 class="fs_1">Contacts</h5>
          </a>
        </li>
        <li class="w_30 d_flex flex_between ml-32">
          <div></div>
          <a href="#" class="p-16 d_flex align_center">
              <input class="border_search align_self_end mb-16">
              <i type="submit" class="fas fa-search"></i>
          </a>
          <div class="mr-32"></div>
        </li>
      </ul>
    </nav>

  </div>

</template>

<script>

export default {
  name: 'HeaderComp',
  components: {
    
  }
}
</script>

<style lang="scss">
@import '../assets/style/sass/app.scss';


   // Font
   .montserrat-bold {
      font-family: 'Montserrat-Bold', sans-serif;
   }

   nav{
      position: fixed;
      z-index: 100;
      background-color: white;
   }


   a{
      color: black;
   }

   a:hover{
         cursor: pointer;
         color: #a7a8b1;
      }
  

  input:hover{
      cursor: pointer;
       color: #a7a8b1;
    }

  button:hover{
    cursor: pointer;
      color: #a7a8b1;
  }

</style>
