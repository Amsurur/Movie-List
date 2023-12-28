<template lang="">
  <div> <ul class="mt-[2rem] text-lg font-semibold p-[1.5rem] bg-[#fcfaf5] shadow-xl
  rounded" > <MovieListItem v-for="movie in movies" :movie="movie" :key="movie.id" />
  </ul> </div>
</template>
<script>
import MovieListItem from "../MovieListItem/MovieListItem.vue";
export default {
  components: {
    MovieListItem,
  },
  props: {
    movies: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style lang=""></style>
