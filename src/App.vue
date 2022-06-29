<template>
  <div>
    Hello {{ greet }}, You are viewing {{ name }}
  </div>
  <p></p>
  <hr/>

</template>

<script>
export default {
  name: 'App',
  data() {    
    return {
      'greet': 'Good Afternoon',
      name:' Vue App',
    };
  },
  methods: {
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

hr {
  border: 2px solid #035891;
}
</style>
