<template>
  <div>
    <h4>App Component Text</h4>
    <child-style>
      <h4>Parent tag text</h4>
    </child-style>
  </div>
</template>

<script>
import ChildStyle from './components/ChildStyle.vue';
  export default {
    components: { 
      ChildStyle 
    },
    
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

h4 {
  color: orange;
}
</style>