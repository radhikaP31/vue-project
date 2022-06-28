<template>
  <div> Hello {{greet }}, You are viewing {{ name }},Here is some example of Bonus Directives </div>
  <p> v-once, v-pre, </p>
  <hr>
  <h2 v-once>{{ fullName }}</h2>
  <button @click="fullName = 'Batman'"> Change Name (On Click)</button>
  <h2 v-pre> {{ fullName }}</h2>

</template>

<script>
export default {
  name: 'App',
  data() {    
    return {
      'greet': 'Good Afternoon',
      name:' Vue App',
      fullName: 'Spiderman',
    };
  },
  methods: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

hr{
  border: 2px solid #035891;
}
</style>
