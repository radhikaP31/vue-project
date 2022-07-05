<template>
  <h2>toRefs example</h2>
  <div>
    <demo-two-component />
  </div>
  <hr />
</template>

<script>
import DemoTwoComponent from "./components/DemoTwoComponent.vue";

export default {
  name: "App",
  components: {
    DemoTwoComponent,
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