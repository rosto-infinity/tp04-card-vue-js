<template>
  <div class="px-[60px] pb-7 border-2 border-green-10 rounded-xl cursor-pointer pt-12">
    <img :src="img" :alt="title" class="max-w-[150px] w-full rounded-xl  mx-auto mb-4" />
    <h2 class="text-2xl text-center">{{ title }}</h2>
  </div>
</template>

<script setup lang="ts">
const props=defineProps<{
  title: string,
  img: string
}>();
</script>

<style scoped></style>