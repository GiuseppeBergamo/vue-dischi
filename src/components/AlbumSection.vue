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
import axios from 'axios';
import AlbumCard from './AlbumCard.vue';
export default {
    name: 'AlbumSection',
    components: {
        AlbumCard,
    },
    data(){
        return {
            albums: []
        }
    },
    mounted(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((res) => {
            this.albums = res.data.response;
        })
    }
}
</script>

<style>

</style>