<template>
  <button class="bg-green-500 hover:bg-green-700 duration-150 py-2.5 px-10 rounded-lg text-lg font-medium">
  <slot>
    {{ label }}
  </slot>
  </button>
</template>

<script setup lang="ts">
defineProps<{
  label:string
}>();

</script>

<style scoped>

</style>