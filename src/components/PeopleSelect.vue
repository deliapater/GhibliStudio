<template lang="html">
  <div>
    <label>Select People</label>
    <select v-on:change="handleSelectPeople" v-model="selectedPerson" id="person-selected">
      <option disable value="">Select People</option>
      <option v-for="(person,index) in people":value="index">{{people.name}}</option>
    </select>
  </div>
</template>


<script>

import { eventBus } from '../main.js'
export default {
  name: 'person-select',
  data(){
    return {
      selectedPerson: ''
    }
  },
  props: ['pleople'],
  methods: {
    "handleSelectPeople": function(){
      eventBus.$emit('people-selected', this.selectedPeople)
    }

  }
}
</script>

<style lang="css" scoped>


</style>
