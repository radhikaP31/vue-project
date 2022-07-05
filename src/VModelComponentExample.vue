<template>
  <h2>v-model and Composition API</h2>
  <hr />
  <div>
    <v-model />
  </div>
</template>

<script>
import VModel from "./components/VModel.vue";

export default {
  name: "App",
  components: {
    VModel,
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