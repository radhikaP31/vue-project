<template>
  <h2>Replacing Watchers</h2>
  <hr />
  <div>
    <WatcherComponent />
  </div>
</template>

<script>
import WatcherComponent from "./components/WatcherComponent.vue";

export default {
  name: "App",
  components: {
    WatcherComponent,
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