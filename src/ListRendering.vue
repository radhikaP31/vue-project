<template>
  <div> Hello {{greet }}, You are viewing {{ name }}, Here is some example of List Rendering.. </div>

  <hr>

  <h2> This is example of render list element with v-for and :key</h2>
  <p v-for="(name,index) in names" :key="name">{{ index }} - {{ name }} </p>

  <hr>

    <h2> This is example of render list key,value array with v-for </h2>

    <p v-for="name in fullNames" :key="name.first">Full Name: {{ name.first }} {{ name.lastname }} </p>

  <hr>

  <h2> This is example of render list key,value array with v-for </h2>

  <p v-for="actor in actors" :key="actor.name">
    <b>{{ actor.name}}</b> <br>
    Movies: <span v-for="movie in actor.movies" :key="movie"> {{ movie }},</span>
  </p>

  <hr>
  <h2> Print key, value and index</h2>
  <h5 v-for="(value, key, index) in myInfo" :key="value"> {{index}} - {{key}} : {{value}} </h5>
  <hr>

</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      'greet': 'Good Afternoon',
      name:' Vue App',
      names: ['Thor', 'Hulk' , 'Ironman'],
      fullNames: [
        {'first': 'Thor', 'lastname': 'Rock'},
        {'first': 'Hulk', 'lastname': 'Dia'},
        {'first': 'Ironman', 'lastname': 'Toy'},
      ],
      actors:[
        {
          'name': 'Christian Bale',
          'movies': ['Batman', 'The Prestige'],
        },
        {
          'name': 'Di Caprio',
          'movies': ['Titanic', 'Inception'],
        },
      ],
      myInfo: {
        name: 'Superia',
        course: 'Vue Js',
        duration: 'Month',
      }
    };
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

hr{
  border: 2px solid #035891;
}
</style>
