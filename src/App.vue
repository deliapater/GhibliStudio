<template lang="html">
  <div class="background">
    <h1>Studio Ghibli</h1>
    <div class="main-container">
      <film-select :films = "films"></film-select>
      <film-details :film = "selectedFilm"></film-details>
    </div>
  </div>
</template>

<script>
import FilmsSelect from './components/FilmsSelect.vue';
import FilmDetails from './components/FilmDetails.vue';
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

h1 {
  text-align: center;
  font-family: fantasy;
  font-size: 50px;
}

</style>
