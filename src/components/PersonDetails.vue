<template lang="html">
<div v-if="person" class="info-container-2">
  <h1>{{person.name}}</h1>
  <p>{{person.gender}}</p>
  <p>{{person.age}}</p>

</div>
</template>

<script>
export default {
  name: 'person-details',
  props: ['person'],

}
</script>

<style lang="css" scoped>


</style>
