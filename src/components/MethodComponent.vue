<template>
  <div>
    <h2>{{ name }}</h2>
    <button @click="changeName">Change Name</button>

    <h2>{{ count }}</h2>
    <button @click="incrementCount">Increment Count</button>

    <h2>{{ first }} {{ last }}</h2>
    <button @click="changeHero">Change Hero</button>
  </div>
</template>

<script>
import { ref, reactive, toRefs } from "vue";
export default {
  name: "MethodComponent",
  setup() {
    const count = ref(0);

    function incrementCount() {
      count.value++;
    }

    const state = reactive({
      first: "Peter",
      last: "Parker",
    });
    function changeHero() {
      state.first = "Tony";
      state.last = "Stark";
    }

    return {
      count,
      incrementCount,
      changeHero,
      ...toRefs(state),
    };
  },
  data() {
    return {
      name: "Spiderman",
    };
  },
  methods: {
    changeName() {
      this.name = "Batman";
    },
  },
};
</script>

<style lang="scss" scoped>
</style>