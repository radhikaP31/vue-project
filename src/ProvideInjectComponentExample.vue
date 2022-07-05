<template>
  <h2>Replacing Provide/Inject</h2>
  <hr />
  <div>
    <ProvideInject />
  </div>
</template>

<script>
import ProvideInject from "./components/ProvideInject.vue";

export default {
  name: "App",
  components: {
    ProvideInject,
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