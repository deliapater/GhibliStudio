<template lang="html">
  <div>
    <h1>Studio Ghibli</h1>
    <div class="main-container">
      <film-select :films = "films"></film-select>
      <film-details :film = "selectedFilm"></film-details>
      <div v-if="film">
      <person-select :people = "people"></person-select>
      <person-details :person = "selectedPerson"></person-details>
    </div>
    </div>
  </div>
</template>

<script>
import FilmsSelect from './components/FilmsSelect.vue';
import FilmDetails from './components/FilmDetails.vue';
import PeopleSelect from './components/PeopleSelect.vue';
import PersonDetails from './components/PersonDetails.vue';
import {eventBus} from './main.js';


export default {
  data(){
    return {
      films: [],
      selectedFilm: null,
      people: [],
      selectPerson: null,
    }
  },
  components: {
    'film-select': FilmsSelect,
    'film-details': FilmDetails,
    'person-select': PeopleSelect,
    'person-details': PersonDetails,

  },
  mounted(){
    fetch('https://ghibliapi.herokuapp.com/films')
    .then(res => res.json())
    .then(films => this.films = films)
    eventBus.$on('film-selected', (index) => {
      this.selectedFilm = this.films[index];
    }),

    fetch('https://ghibliapi.herokuapp.com/people')
    .then(res => res.json())
    .then(people => this.people = people)
      eventBus.$on('person-selected', (index) => {
      this.selectedPerson = this.people[index];
    })
  }
}
</script>

<style lang="css" scoped>
  .main-container {
    display: flex;
    justify-content: center;
  }


</style>
