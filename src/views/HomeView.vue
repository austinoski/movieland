<template>
  <Search @search="searchMovie" />
  <Movies :movies="movies" />
</template>

<script>
import Search from '../components/Search.vue'
import Movies from '../components/Movies.vue'

export default {
  name: 'HomeView',
  components: {
    Search,
    Movies
  },
  data() {
    return {
        movies: [],
        API_URL: 'https://www.omdbapi.com?apikey=11fb7995',
        default: "Harry Potter"
    }
  },
  methods: {
    async searchMovie(title) {
      const response = await fetch(`${this.API_URL}&s=${title}`)
    const data = await response.json()
    this.movies = data.Search
    console.log(data.Search)
    }
  },
  async created(){
    const response = await fetch(`${this.API_URL}&s=${this.default}`)
    const data = await response.json()
    this.movies = data.Search
  }
}
</script>
