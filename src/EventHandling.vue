<template>
  <div> Hello {{greet }}, You are viewing {{ name }},Here is some example of Event Handling </div>
  <hr>
  <h2> Its change the name onclick of button event</h2>
  <h2> {{ name }}</h2>
  <div>
    <button v-on:click="name = 'Batman'"> Change Name (On Click)</button>
    <button v-on:mouseover="name = 'Batman'"> Change Name (On Hover)</button>
  </div>

  <hr>
  <h2> Its change the name onclick of button event with method call</h2>
  <h2> {{ name }}</h2>
  <div>
    <button v-on:click="changeName"> Change Name (On Click with method)</button>
  </div>

  <hr>
  <h2> Example of multiple event call</h2>
  <h2> {{ name }}</h2>
  <div>
    <button v-on:click="changeName($event), increment(2, $event)"> Change Name (On Click with method)</button>
  </div>

  <hr>
  <h2> Its change the counter onclick of button event</h2>
  <h2> {{ count }}</h2>
  <div>
    <button v-on:click="count += 1">Increment</button>
    <button v-on:click="count -= 1">Decrement</button>
  </div>

  <hr>
  <h2> Its change the counter onclick of button with method call with number parameter</h2>
  <h2> {{ count1 }}</h2>
  <div>
    <button @click="increment(1, $event)">Increment 1</button>
    <button @click="decrement(1)">Decrement 1</button>
    <button @click="increment(10)">Increment 10</button>
    <button @click="decrement(5)">Decrement 5</button>
  </div>

</template>

<script>
export default {
  name: 'App',
  data() {    
    return {
      'greet': 'Good Afternoon',
      name:' Vue App',
      count: 0,
      count1: 0,
    };
  },
  methods: {
    changeName(event) {
      this.name = 'Batman'
      console.log('Event',event)
    },
    increment(num, event){
      this.count1 += num
      console.log('Event',event)
    },
    decrement(num){
      this.count1 -= num
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
