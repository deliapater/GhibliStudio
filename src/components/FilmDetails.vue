<template lang="html">
<div v-if="film" class="info-container">
  <h1>{{film.title}}</h1>
  <h4>{{film.description}}</h4>
  <p>Director: {{film.director}}</p>
  <p>Producer: {{film.producer}}</p>
  <p>Realase Date: {{film.release_date}}</p>

</div>
</template>

<script>
export default {
  name: 'film-details',
  props: ['film'],

}
</script>

<style lang="css" scoped>


</style>
