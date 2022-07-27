<template>
  <header class="container-fluid py-1 d-flex justify-content-between">
    <img src="https://th.bing.com/th/id/R.2ebc6c77ba84d7194d4a8f6a7334571e?rik=2ffoY4RHjXWJ2w&pid=ImgRaw&r=0" alt="spotify-logo" class="img-fluid">
    <BaseSelect :options="options"></BaseSelect>
  </header>
</template>

<script>
import BaseSelect from "./BaseSelect.vue";
export default {
    name: "BaseHeader",
    data(){
      return {
        options: [
          {
            id: 1,
            text: "Scegli il genere",
            genre: "Scegli il genere"
          },
          {
            id: 2,
            text: "Metal",
            genre: "Metal"
          },
          {
            id: 3,
            text: "Jazz",
            genre: "Jazz"
          },
          {
            id: 4,
            text: "Pop",
            genre: "Pop"
          },
          {
            id: 5,
            text: "Rock",
            genre: "Rock"
          }
        ]
      }
    },
    props: {
        albums: Array
    },
    components: { BaseSelect }
}
</script>

<style scoped>
    header{
        height: 50px;
        background-color: #2e3a46;
    }
</style>