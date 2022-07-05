<template>
  <h2>Replacing Computed Properties</h2>
  <hr />
  <div>
    <ComputedComponent />
  </div>
</template>

<script>
import ComputedComponent from "./components/ComputedComponent.vue";

export default {
  name: "App",
  components: {
    ComputedComponent,
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