<template>
  <a :href="to"
     class="p-3 m-6  justify-center min-w-[300px] rounded shadow-[6px_6px_1px_2px_rgba(0,0,0,.9)] hover:shadow-[6px_6px_1px_2px_rgba(0,0,0,.2)] hover:text-black/60 transition hover:scale-[105%] flex items-center"
     :class="[color]"
     target="_blank">
    <div class="min-h-[50px] grid place-content-center">
      <img :src="image" width="50px" height="50px" class="mr-4"></img>
    </div>
    <div class="font-bold text-xl">{{ name }}</div>
  </a>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps(['to', 'name', 'color', 'image'])
</script>
