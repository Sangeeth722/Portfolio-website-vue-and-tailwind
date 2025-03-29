<script setup>

import { ref } from 'vue';

const darkModeToggle = ref(new URL('@/assets/images/light-bulb-of.png',import.meta.url).href)

const toggle = ref(false)

const toggleChange=  ()=>{

      toggle.value = !toggle.value
      if (toggle.value){
        darkModeToggle.value = new URL('@/assets/images/light-bulb-on.png',import.meta.url).href
      }else {
        darkModeToggle.value = new URL('@/assets/images/light-bulb-of.png',import.meta.url).href
      }

}
</script>




<template>
  <div :class="toggle ? 'bg-black text-white':'bg-white text-black' " class=" transition-all duration-700 ">
    <div class=" grid md:grid-cols-2 grid-cols-1">
    <div class=" grid grid-cols-1 border-r-2 border-gray-400">

      <div class="  border-gray-400 border-b-2">
        <img :src="darkModeToggle" class=" w-10 h-10  cursor-pointer"  alt="" @click="toggleChange">

        
        <div class=" grid grid-cols-1 md:mt-16 mt-10">
          <!-- profile picture -->
          <img src="/src/assets/images/profile-icture.jpg" alt="profilepicture" class=" w-60 h-60 rounded-full md:ml-52 ml-14">
          
          <!-- Name -->
           <span class=" md:ml-36 md:text-4xl text-lg ml-20 md:mt-6 mt-2 font-bold text-blue-500">Martha Belivins (she/her)</span>
           <span class=" md:text-2xl text-base md:ml-60 md:mt-2 text-blue-500 font-bold ml-28 md:mb-12 mb-6">ARTS TEACHER</span>
           

        </div>
      <!-- profile -->
      </div>

      <div class=" grid grid-cols-1 md:mt-12 mt-6 md:pb-20 ">
        <!-- connecte wirh me -->
         <div>
          <span class=" text-blue-500 font-semibold md:ml-60 ml-28 md:text-xl text-base">
            CONNECT WITH ME
          </span>
          <!-- Logos -->
          <div class=" mt-3 md:ml-52 md:mt-3  ml-16">

            
              <a href="">
              <img src="/src/assets/images/Home.png" alt="" class="">
            </a>
            
          
            

          </div>
         </div>

      </div>
    </div>
    <!-- about me -->

    <div class=" grid grid-cols-1 md:flex md:flex-col">
      <div class=" flex flex-col mt-16 md:ml-20 ml-2">
        <span class="text-blue-500 font-semibold text-xl">ABOUT ME</span>
        <span class=" text-2xl mt-1 text-blue-500 font-semibold">Art changes us</span>
        <span class=" text-lg font-stretch-expanded leading-relaxed  tracking-wide mt-2 mx-w-lg break-words pb-4 md:pb-11">
          I am a high school art teacher with years of experience  
          in teaching art history and managing challenging  
          classroom environments. I am eager to share my  
        expert knowledge in photography, graphic design, and new media.
        </span>
      </div>

      <div class=" border-gray-400 border-t-2 md:pt-9 pt-2 md:pl-20 pl-2">
        <span class=" text-blue-500 font-semibold text-xl">EXPERIANCE</span>

        <div class=" flex flex-row font-bold md:mt-10 mt-2">
          <span class=" mx-4">2018</span>
          <div class=" flex flex-col">
            <span>HIGH SCHOOL TEACHER</span>
            <span class=" font-normal md:mt-2">Cordel High School </span>

          </div>

          
          

        </div>

        <div class=" md:mt-12 mt-3">

        <span class=" text-blue-500 font-semibold text-xl">EDUCATION</span>

        <div class=" flex flex-col md:flex-row font-bold md:mt-9 md:pl-6 pl-3 mt-2">
          <span class=" mb-2">2006</span>
          
          <div class=" flex flex-col">
            <span class=" md:ml-9 ">Master of Fine Arts in Photography and New Media</span>
            <span class=" font-normal md:ml-9 md:mt-2">Tresswood University <br>

              Phyllis Schwaiger Memorial Award</span>

          </div>
          
        </div>
        </div>

      </div>
    </div>

  </div>

  </div>

  



  
</template>

<style>


</style>