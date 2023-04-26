<script setup>
import { items } from "./movies.json";
/*
 This is an Icon that you can use to represent the stars if you like
 otherwise you could just use a simple ⭐️ emoji, or * character.
*/
import { StarIcon } from "@heroicons/vue/24/solid";
</script>

<template>
  <!-- This is where your template goes	-->
  <div class="flex justify-center w-full py-4 px-12">
    <div class="grid grid-cols-4 gap-8">
      <div class="flex flex-col m-4" v-for="item in items">
        <img class="h-1/2" :src="item.image">
        <div class="flex-1 flex flex-col p-4 bg-white">
          <div class="font-bold">{{ item.name }}</div>
          <div class="py-2 mt-2">
            <span class="rounded-xl bg-blue-700 text-white m-1 p-1" v-for="genre in item.genres">{{ genre }}</span>
          </div>
          <div class="flex-1 mt-2">{{ item.description }}</div>
          <div class="flex flex-nowrap mt-4">
            Rating ({{ item.rating }}/5)
            <span class="flex flex-nowrap ml-2">
              <StarIcon v-for="index in item.rating" class="text-amber-300 w-6" />
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
