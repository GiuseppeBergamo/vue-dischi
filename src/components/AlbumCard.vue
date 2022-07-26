<template>
    <div id="album-card" class="text-center p-2 text-white">
        <img :src="poster" :alt="title" class="img-fluid mb-2">
        <h3 id="title" class="fw-bold text-uppercase">{{ title }}</h3>
        <div id="author" class="text-muted">
            <p class="m-0">{{ author }}</p>
            <p class="m-0">{{ year }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AlbumCard',
    props: {
        title: String,
        poster: String,
        author: String,
        genre: String,
        year: String
    }
}
</script>

<style scoped>
    #album-card {
        background-color: #2e3a46;
        height: 400px;
    }
</style>