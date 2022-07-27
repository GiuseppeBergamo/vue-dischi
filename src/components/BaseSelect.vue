<template>
  <select>
    <option v-for="genre in albums" :key="album.title" v-model=""></option>
  </select>
</template>

<script>
export default {
    name: 'BaseSelect',
    props: {
        albums: Array
    }
}
</script>

<style>

</style>