<template>
  <div id="app">
    <BaseHeader></BaseHeader>
    <TheMain></TheMain>
  </div>
</template>

<script>
import BaseHeader from './components/BaseHeader.vue';
import TheMain from './components/TheMain.vue';

export default {
  name: 'App',
  components: {
    BaseHeader,
    TheMain
}
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
