<template lang="html">
  <div>
    <select v-on:change="handleSelect" v-model="selectedFilm" id="film-selected">
      <option disable value="">Select a Film</option>
      <option v-for="(film,index) in films":value="index">{{film.title}}</option>
    </select>
  </div>
</template>

<script>

import { eventBus } from '../main.js'
export default {
  name: 'film-select',
  data(){
    return {
      selectedFilm: ''
    }
  },

  props: ['films'],
  methods: {
    "handleSelect": function(){
      eventBus.$emit('film-selected', this.selectedFilm)
    }

  }
}
</script>

<style lang="css" scoped>


</style>
