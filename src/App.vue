<script setup>
import { items } from "./movies.json";
/*
 This is an Icon that you can use to represent the stars if you like
 otherwise you could just use a simple ⭐️ emoji, or * character.
*/
// import { StarIcon } from "@heroicons/vue/24/solid";
</script>

<template>
  <!-- This is where your template goes	-->
  <div class="flex justify-center w-full py-4">
    <div class="grid grid-cols-4 gap-8">
      <div v-for="item in items">
        <img class="w-72 h-96" :src="item.image">
      </div>
    </div>
  </div>
</template>
