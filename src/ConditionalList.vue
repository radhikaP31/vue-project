<template>
  <div> Hello {{greet }}, You are viewing {{ name }},Here is some example of Conditional List Rendering.. (:key) </div>

  <hr>

  <h2> This is example of render list element with v-for and :key</h2>
  <template v-for="name in names" :key="name"> 
    <h5 v-if="name === 'Hulk'"> {{ name }}</h5>
  </template>

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
