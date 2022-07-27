<template>
  <main>
    <div class="container py-4">
        <AlbumSection :albums="albums"></AlbumSection>
    </div>
  </main>
</template>

<script>
import AlbumSection from './AlbumSection.vue';
export default {
    name: 'TheMain',
    components: {
        AlbumSection,
    },
    props: {
        albums: Array
    }
}
</script>

<style scoped>
    main{
        background-color: #1e2d3b;
    }
</style>