<template>
  <h2>ref() Example</h2>
  <div>
    <demo-one-component />
  </div>
  <hr />
</template>

<script>
import DemoOneComponent from "./components/DemoOneComponent.vue";

export default {
  name: "App",
  components: {
    DemoOneComponent,
  },
};
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