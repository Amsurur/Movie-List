<template>
  <div
    class="flex item-center m-1 shadow-xl p-2 rounded"
    :class="[{ 'bg-white': movie.like }, { 'text-blue-400': movie.favorites }]"
  >
    <span>{{ movie.title }}</span>
    <img class="w-[100px] h-[50px] object-cover mx-5" :src="movie.image" alt="" />
    <input
      type="number"
      class="border-none outline-none m-1 rounded text-center"
      :value="movie.views"
    />
    <div class="flex justify-center items-center">
      <button class="border bg-yellow-200">Cookie</button>
      <button class="border bg-red-400">Del</button>
      <button class="border bg-orange-400 transition">Fav</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    movie: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style>
/* Add your styles here */
</style>
