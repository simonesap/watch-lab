<template>

  <div class="w_100 bg_white">

    <nav class="w_100">
      <ul class="d_flex flex_between m_0">
        <li class="w_80 d_flex flex_between align_center m_0 montserrat-bold ">
          <a href="#" class="bg_beige p-16 m_0 text_uppercase mt-32 ml-32 d_flex align_center">
             <h3 class="text_white fs_1_08">watch/lab</h3>
          </a>
          <a href="#" class="p-16 d_flex align_center d_none_1074">
             <h5 class="fs_1 fs_1_04_950">About us</h5>
          </a>
          <a href="#" class="p-16 d_flex align_center d_none_560px">
             <h5 class="fs_1">Brand</h5>
          </a>
          <a href="#" class="p-16 d_flex align_center d_none_560px">
             <h5 class="fs_1">Projects</h5>
          </a>
          <a href="#" class="p-16 d_flex align_center d_none_560px">
             <h5 class="fs_1">Magazine</h5>
          </a>
          <a href="#" class="p-16 d_flex align_center d_none_560px">
             <h5 class="fs_1">Press</h5>
          </a>
          <a href="#" class="p-16 d_flex align_center d_none_806">
             <h5 class="fs_1">Contacts</h5>
          </a>
        </li>
        <li class="w_30 d_flex flex_between ml-32">
          <div></div>
          <a href="#" class="p-16 d_flex align_center d_none_560px">
              <input class="border_search align_self_end mb-16">
              <i type="submit" class="fas fa-search"></i>
          </a>

         <!-- Dropdown -->
         <!-- <div class="dropdown">
            <span>
               <i class="fa-solid fa-bars"></i>
            </span>
            <div class="dropdown-content">
               <a href="#" class="p-16 d_flex align_center">
                  <h5 class="fs_1">Brand</h5>
               </a>
               <a href="#" class="p-16 d_flex align_center">
                  <h5 class="fs_1">Projects</h5>
               </a>
            </div>
         </div> -->
         <select v-model="selectedValue" name="LeaveType" :onchange="onChange(this.value)" class="custom-select d_none_2766 d_none_2200 d_none_2000 d_none_1615 d_none_1440 d_none_1248 d_none_1128 d_none_1074 d_none_1024 d_none_950 d_none_806 d_none_769px d_none_744px d_none_674 d_none_640px d_none_600px b_none ml-2 d_block_560px d_block_400px d_block_480px">
         
            <option class="select-items bg_gold b_none bg_gold d_flex align_center" value="1">
               <h5 class="fs_06">Brand</h5>  
            </option> 
            <option class="select-items bg_gold b_none d_flex align_center" value="2">
               <h5 class="fs_6">Projects</h5>
            </option>
            <option class="select-items bg_gold b_none d_flex align_center" value="3">
               <h5 class="fs_6">Magazine</h5>
            </option>
         </select>
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
    
  },

  data(){
   return {
        selectedValue : 1
    }
  },
   

  methods:{
        onChange: function(){
            console.log(this.selectedValue);
        }
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
