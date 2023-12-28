<template>
  <div class="h-[100vh] text-[#000]">
    <div class="bg-[] w-[70%] mx-auto py-[5rem]">
      <AppInfo
        :allMoviesCount="movies.length"
        :favoritesMovieCount="movies.filter((c) => c.favorites).length"
      />
      <div class="mt-[2rem] p-[1.5rem] bg-[#fcfaf5] shadow-xl rounded">
        <SearchPanel />
        <AppFilter />
      </div>
      <MovieList :movies="movies" />
      <movie-add-form />
    </div>
  </div>
</template>

<script>
import AppInfo from "./components/app-info/AppInfo.vue";
import AppFilter from "./components/AppFiler/AppFilter.vue";
import MovieAddForm from "./components/movieAddform/MovieAddForm.vue";
import MovieList from "./components/MovieList/MovieList.vue";
import SearchPanel from "./components/search-panel/SearchPanel.vue";
export default {
  components: {
    AppInfo,
    SearchPanel,
    AppFilter,
    MovieList,
    MovieAddForm,
  },
  data() {
    return {
      movies: [
        {
          id: 1,
          title: "Star Wars: Episode I - The Phantom Menace",
          views: 1232,
          favorites: false,
          like: true,
          image: "img/javascript-sm.png",
        },
        {
          id: 2,
          title: "Star Wars: Episode II - Attack of the Clones",
          views: 123,
          favorites: false,
          like: false,
          image: "img/react-hooks-best-practices-lead_.jpg",
        },
        {
          id: 3,
          title: "Star Wars: Episode III - Revenge of the Sith",
          views: 123,
          favorites: true,
          like: true,
          image: "img/react-js-logo-no-2932x2932.jpg",
        },
      ],
    };
  },
};
</script>
<style></style>
