<template>
  <div> Hello {{greet }}, You are viewing {{ name }},Here is some example of Methods </div>

  <hr>
    <h2> Add two number with add()</h2>
    <h5> Add Number: {{ add(10,25,65) }}</h5>

  <hr>
    <h2> Multiply two number with multiply() with data variable basemultiply</h2>
    <h5> Multiply Number: {{ multiply(10) }}</h5>
  
  <hr>
    <h2> Multiply two number with multiply() with given data variable</h2>
    <h5> Multiply Number: {{ multiply(baseValue) }}</h5>

</template>

<script>
export default {
  name: 'App',
  data() {    
    return {
      'greet': 'Good Afternoon',
      name:' Vue App',
      basemultiply: 5,
      baseValue: 2,
    };
  },
  methods: {
    add(a,b,c) {
      return a + b + c;
    }, 
    multiply(num){
      return num * this.basemultiply
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

hr{
  border: 2px solid #035891;
}
</style>
