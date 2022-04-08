<template>
    <div class="movies">
        <div  :key="movie.imdbID" v-for="movie in movies" class="movie">
            <Movie :movie="movie"/>
        </div>
    </div>
</template>

<script>
import Movie from './Movie.vue'

export default {
    name: 'Movies',
    components: {
        Movie
    },
    props: {
        movies: Array
    }
}
</script>

<style scoped>
    @media(min-width: 768px){
        .movie {
            width: 21%;
            margin: 10px 1%;
        }
    }
    @media(max-width: 768px){
        .movie {
            width: 100%;
            margin: 10px 1%;
        }
    }
    .movies {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        margin-top: 30px;
    }
    .movie {
        border: 1px solid white;
        border-radius: 10px;
    }
</style>
