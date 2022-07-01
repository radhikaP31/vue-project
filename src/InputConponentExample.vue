<template>
  <div>
     Here is a example of Component Events with v-model
  </div>
  <hr/>

   <InputComponent v-model="name"/> 
</template>

<script>
import InputComponent from './components/InputComponent.vue'

export default {
  name: 'App',
  components: {
    InputComponent
  },
  data(){
    return {
      name: '',
    }
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
