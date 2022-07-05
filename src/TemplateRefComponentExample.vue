<template>
  <h2> Template Refs and Composition API</h2>
  <hr />
  <div>
    <TemplateRefComponent />
  </div>
</template>

<script>
import TemplateRefComponent from "./components/TemplateRefComponent.vue";

export default {
  name: "App",
  components: {
    TemplateRefComponent,
  },
};
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