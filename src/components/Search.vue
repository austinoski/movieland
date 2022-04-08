<template>
    <form class="search" method="post">
        <input type="text" v-model="title" placeholder="Search Movie Title">
        <button @click.prevent="search">Search</button>
    </form>
</template>

<script>
export default {
    name: 'Search',
    data() {
        return {
            title: String("Harry Potter")
        }
    },
    methods: {
        search() {
            this.$emit('search', this.title)
        }
    }
}
</script>

<style scoped>
    .search {
        display: flex;
        flex-direction: row;
    }

    .search button {
        flex: 1;
        background-color: skyblue;
        border: 1px solid skyblue;
        border-radius: 5px;
        margin-left: 2px;
    }

    input {
        width: 90%;
        height: 25px;
        border: 1px solid black;
        border-radius: 5px;
    }
</style>
