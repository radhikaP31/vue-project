<template>
  App Component App name - {{name}}
  <component-c/>
</template>

<script>
import ComponentC from './components/ComponentC.vue'
  export default {
      name:'App',
      components: {
        ComponentC
      },
      data() {
        return {
          name: 'Vue',
        }
      },
      provide() {
        return {
          appname: this.name
        }
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

</style>