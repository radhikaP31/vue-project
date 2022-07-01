<template>
  <div>
    <card-component></card-component>
    <card-component>Card Content with string</card-component>
    <card-component>
      <h2>Test Card with html tags </h2>
    </card-component>
    <card-component>
      <img src="https://picsum.photos/200" />
    </card-component>

    <card-component>
      <template v-slot:header>
        <h3>Card Header</h3>
      </template>
      <template v-slot:default>
        <img src="https://picsum.photos/200" />
      </template>
      <template v-slot:footer>
        <button>View Details</button>
      </template>
    </card-component>
  </div>
</template>

<script>
import CardComponent from './components/CardComponent.vue';
  export default {
    name: 'App',
    components: {
      CardComponent
    },
    data() {
      return{

      }
    }
  }
</script>

<style lang="scss" scoped>

</style>