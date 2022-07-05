<template>
  <h2>Reusability with Composition API</h2>
  <hr />
  <div>
    <click-counter-component/>
    <hover-counter-component/>
  </div>
</template>

<script>
import ClickCounterComponent from './components/ClickCounterComponent.vue'
import HoverCounterComponent from './components/HoverCounterComponent.vue'

  export default {
    name: 'App',
    components: {
        ClickCounterComponent,
        HoverCounterComponent
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
</style>`