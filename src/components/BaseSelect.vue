<template>
  <select>
    <option v-for="option in options" :key="option.id" :value="option.genre">{{option.text}}</option>
  </select>
</template>

<script>
export default {
    name: 'BaseSelect',
    props: {
        options: Array
    },
    
}
</script>

<style>

</style>