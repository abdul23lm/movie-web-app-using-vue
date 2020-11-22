<template>
  <div id="movie-container">
      Movie List
      <ul>
          <li 
          style="color: white" 
          v-for="(movie, index) in movies" 
          :key="movie.id"
          >
            Index: {{ index }}: {{ movie.name }}</li>
      </ul>
  </div>    
</template>

<script>
export default {
    data() {
        return {
            movies: [],
        };
    },
    computed: {
    //     movies() {
    //         return this.$store.getters.getMovies;
    // },
    },
    created(){
        this.movies = this.$store.getters.getMovies
    }
};
</script>

<style lang='scss' scoped>
	#movie-container {
		padding-top: 1rem;
		display: flex;
		flex-wrap: wrap;
		flex-grow: 2;
		justify-content: center;
	}
</style>