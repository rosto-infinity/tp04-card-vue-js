<template>
  <div class="min-h-screen bg-slate-300 flex justify-center items-center px-14 py-20">
    <div class="w-full py-24 mx-auto flex flex-col items-center shadow-lg rounded-lg bg-white">
      <h1 class="text-3xl mb-6">Select your role </h1>
      <p class="mb-10 sm:p-6">
        To start your project we need to know your role in the project. Please select one of the following options.
      </p>
      
      <div class="flex p-9 gap-10">
        <RoleCard  v-for="(role,index) in roles"
        :key="role.title" :img="role.img" :alt="role.title" :title="role.title"
        :active="role.active"
       @click="selectRole(index)"
      
        />
      </div>
        <div class="flex gap-1">
         <div v-for="n in 4"
         :key="n" 
         :class="{'!bg-green-400':n===3}"
         class="d w-3 h-3 bg-slate-400 rounded-full cursor-pointer"></div>
         </div>
     
         <BaseButton label="label" class="mt-7">
          Suivant <i class="fas fa-arrow-right animate-ping text-white" </i>
         </BaseButton>
         
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import RoleCard from './components/RoleCard.vue';
import BaseButton from './components/BaseButton.vue';

import Develop from './assets/team-01.png'
import Img from './assets/team-02.png'
import SoftIng from './assets/team-03.png'


const roles = ref([
  { title: 'Developer', img: Develop, active: false },
  { title: 'Designer Graphic', img: Img, active: false },
  { title: 'Software Engineer', img: SoftIng, active: false },
]);

const selectRole = (index:number) => {
  roles.value.forEach((role)=>(role.active =false));
  roles.value[index].active =true;
}
</script>

<style scoped>
         </style>