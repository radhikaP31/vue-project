<template>
  <div>
    <data-component/>
  </div>
  <hr/>

</template>

<script>
import DataComponent from './components/DataComponent.vue'

  export default {
    name: 'App',
    components: {
        DataComponent

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