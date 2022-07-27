<template>
  <section id="album-section">
    <div id="album-list" class="row row-cols-5 gy-4">
        <div class="col" v-for="album in albums" :key="album.author">
            <AlbumCard :title="album.title" :poster="album.poster" :author="album.author" :genre="album.genre" :year="album.year"></AlbumCard>
        </div>
    </div>
  </section>
</template>

<script>
import AlbumCard from './AlbumCard.vue';
export default {
    name: 'AlbumSection',
    components: {
        AlbumCard,
    },
    props: {
        albums: Array
    }
}
</script>

<style>

</style>