<template>
  <div>
    Hello {{ name }}, You are viewing {{ name }}, Here is a example of Template Refs
  </div>
  <hr/>
  <TemplateRef />

</template>

<script>
import TemplateRef from './components/TemplateRef.vue'

export default {
  name: 'App',
  components: {
    TemplateRef
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
