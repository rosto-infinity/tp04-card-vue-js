<template>
  <div class="min-h-screen bg-slate-300 flex justify-center items-center px-14 py-20">
    <div class="w-full py-24 mx-auto flex flex-col items-center shadow-lg rounded-lg bg-white">
      <h1 class="text-3xl mb-6">Select your role </h1>
      <p class="mb-10 sm:p-6">
        To start your project we need to know your role in the project. Please select one of the following options.
      </p>
      
      <div class="flex p-9 gap-10">
        <RoleCard  v-for="role in roles"
        :key="role.title" :img="role.img" :alt="role.title" :title="role.title"/>
      </div>


     <!-- <RoleCard :img="roles.img"/> -->
     
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import RoleCard from './components/RoleCard.vue'
import Img from './assets/team-01.png';
import Develop from './assets/team-02.png';
import SoftIng from './assets/team-03.png';
import SoftIng2 from './assets/team-03.png';

const roles =ref([
  {title :'Developer' , img :Develop},
  {title :'Designer Graphic' , img :Img},
  {title :'Software Engineer' , img :SoftIng},
  {title :'Software Engineer2' , img :SoftIng2},
]);
</script>

<style scoped></style>