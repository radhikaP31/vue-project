<template>
  <div>
    Example of Teleport
  </div>
  <hr/>

  <button id="show-modal" @click="showModal = true">Show Modal</button>

  <Teleport to="body">
    <!-- use the modal component, pass in the prop -->
    <modelComponent :show="showModal" @close="showModal = false">
      <template #header>
        <h3>custom header</h3>
      </template>
    </modelComponent>
  </Teleport>

</template>

<script>
  import ModelComponent from './components/ModelComponent.vue'

  export default {
    components: {
      ModelComponent
    },
    data() {
      return {
        showModal: false
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

hr {
  border: 2px solid #035891;
}

</style>