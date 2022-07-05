<template>
  <div>
    <click-counter/>
    <hover-counter/>
  </div>
  <hr/>

</template>

<script>
import ClickCounter from './components/ClickCounter.vue'
import HoverCounter from './components/HoverCounter.vue'

  export default {
    name: 'App',
    components: {
        ClickCounter,
        HoverCounter
    }
  }
</script>

<style scoped>

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