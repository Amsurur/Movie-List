<template>
  <div class="p-[1.5rem] rounded shadow-xl bg-[#fcfaf5]">
    <p class="text-lg">Some Movies: {{ allMoviesCount }}</p>
    <p class="text-lg">Some watched Movies {{ favoritesMovieCount }}</p>
  </div>
</template>
<script>
export default {
  props: {
    allMoviesCount: {
      type: Number,
      required: true,
    },
    favoritesMovieCount: {
      type: Number,
      required: true,
    },
  },
};
</script>
<style></style>
