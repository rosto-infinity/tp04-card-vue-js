<template>
  <div 
  :class="{'border-green-500 shadow-md':active}"
  class="px-[60px] pb-7 border-2 border-green-10 rounded-xl cursor-pointer pt-12">
    <img :src="img" :alt="title" class="max-w-[150px] w-full rounded-xl  mx-auto mb-4" />
    <h2
    :class="{'text-green-500':active}"
     class="text-2xl text-center">{{ title }}</h2>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  title: string;
  img: string;
  active:boolean;
}>();
</script>

<style scoped></style>