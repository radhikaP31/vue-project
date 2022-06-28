<template>
  <div> Hello {{greet }}, You are viewing {{ name }}, , Here is some example of Conditional Statement.. </div>

  <hr>

  <h2><b> This is a example of number is POSITIVE, NEGATIVE or ZERO with use of if-else statement</b></h2>
  <p> The number is {{ num }}:
    <span v-if=" num === 0"> zero.</span>
    <span v-else-if=" num < 0"> negative number</span>
    <span v-else-if=" num > 0"> positive number</span>
    <span v-else> Not a Number.</span>
  </p>

  <hr>

  <h2><b> This is a example of hide multiple tags with use of if-else.</b></h2>
  
  <template v-if="display">

    <span>Vue</span><br>
    <span>Learn</span><br>
    <span>Coding</span><br>

  </template>

  <hr>

  <h2 v-show="showElement">
    This is show example
  </h2>

</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      'greet': 'Good Afternoon',
      name:' Vue App',
      num: 5,
      display:  true,
      showElement: false,
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
