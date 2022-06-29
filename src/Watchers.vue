<template>
  <div>
    Hello {{ greet }}, You are viewing {{ name }},Here is some example of
    Watcher
  </div>
  <p></p>
  <hr/>
  <h2> Volume Tracker (0-20)</h2>
  <h3> Current Volume - {{ volume }}</h3>
  <div>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrease</button>
  </div>
  <hr>
  <input type="text" v-model="movie"><br>
  <input type="text" v-model="movieInfo.title"><br>
  <input type="text" v-model="movieInfo.actor">
  <div>
    <button @click="movieList.push('Wonder Women')"> Add Movie </button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {    
    return {
      'greet': 'Good Afternoon',
      name:' Vue App',
      volume: 0,
      movie: 'Batman',
      movieInfo: {
        title: '',
        actor: '',
      },
      movieList: [ 'Batman', 'Spiderman'],
    };
  },
  methods: {
   
  },
  watch: {
    volume(newValue, oldValue) {
      if(newValue > oldValue && newValue === 16){
        alert('Listing to a high value for a long time may damage your hearing..')
      }
    },
    movie: {
      handler(newValue) {
        console.log(`Call api with movie name: ${newValue}`)
      },
      immediate: true,
    },
    movieInfo: {
      handler(newValue){
        console.log(`Calling api with movie title: ${newValue.title} and actor: ${newValue.actor}`)
      },
      deep: true,
    },
    movieList: {
      handler(newValue) {
        console.log(`Updated List: ${newValue}`)
      },
      deep: true,
    }
  }
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

hr {
  border: 2px solid #035891;
}
</style>
