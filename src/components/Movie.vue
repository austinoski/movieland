<template>
    <img :src="movie.Poster" :alt="movie.Title" />
    <div class="movie-desc">
        <h5>{{ movie.Title }}</h5>
        <p>{{ movie.Type }}</p>
        <p>{{ movie.Year }}</p>
    </div>
</template>

<script>
export default {
    name: 'Movie',
    props: {
        movie: Object
    }
}
</script>

<style scoped>
    img {
        width: 100%;
        height: 250px;
        border-radius: 10px;
    }
    .movie-desc {
        padding: 0px 10px;
        text-align: center;
    }
</style>
