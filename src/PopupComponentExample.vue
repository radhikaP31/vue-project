<template>
  <div>
    Hello {{ name }}, You are viewing {{ name }}, Here is a example of Component Events
  </div>
  <hr/>
  <button @click="showPopup = true"> Show Popup</button>
  <!-- <PopupComponent v-show="showPopup" @close="showPopup = false" /> //for static value change -->
  <PopupComponent v-show="showPopup" @close="closePopup" /> 

</template>

<script>
import PopupComponent from './components/PopupComponent.vue'

export default {
  name: 'App',
  components: {
    PopupComponent
  },
  data(){
    return{
      showPopup: false,
    }
  },
  methods: {
    closePopup(name) {
      console.log('name', name)
      return this.showPopup = false
    }
  }
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
