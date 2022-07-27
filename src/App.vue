<template>
  <div id="app">
    <BaseHeader :albums="albums"></BaseHeader>
    <TheMain :albums="albums"></TheMain>
  </div>
</template>

<script>
import axios from 'axios';
import BaseHeader from './components/BaseHeader.vue';
import TheMain from './components/TheMain.vue';

export default {
  name: 'App',
  components: {
    BaseHeader,
    TheMain
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

<style lang="scss">
@import './assets/scss/style.scss';
</style>
