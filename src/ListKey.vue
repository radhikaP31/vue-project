<template>
  <div> Hello {{greet }}, You are viewing {{ name }},Here is some example of Lists and Keys.. (:key) </div>

  <hr>

    <template v-for="name in names" :key="name">
        <h5>{{ name }} : <input placeholder="Last Name"/></h5>
        
    </template>
    <button @click="shuffle"> Shuffle!! </button>
  <hr>

  
</template>

<script>
import _ from "lodash";
export default {
  name: 'App',
  data() {
    return {
      'greet': 'Good Afternoon',
      name:' Vue App',
      names: ['Thor', 'Hulk' , 'Ironman', 'Captain America'],
    };
  },
  methods: {
    shuffle() {
      console.log(this.names);
      this.names = _.shuffle(this.names);
    },
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
