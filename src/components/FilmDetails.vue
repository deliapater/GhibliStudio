<template lang="html">
<div v-if="film" class="info-container">
  <h1>{{film.title}}</h1>

</div>
</template>

<script>
export default {
  name: 'film-details',
  props: ['film']
}
</script>

<style lang="css" scoped>


</style>
