<template>
  <div>
    <h2>Nomal v-model with Watcher</h2>
    <input type="name" v-model="name" />
    <br /><br />

    <h2>v-model watcher with ref</h2>
    <input type="text" v-model="firstName" placeholder="Firstname" />
    <input type="text" v-model="lastName" placeholder="Lastname" />
    <br /><br />

    <h2>v-model watcher with toRefs</h2>
    <input type="text" v-model="fname" placeholder="Reactive Firstname" />
    <input type="text" v-model="lname" placeholder="Reactive Lastname" />
    <input
      type="text"
      v-model="options.heroName"
      placeholder="Reactive Hero Name"
    />
  </div>
</template>

<script>
import { ref, watch, reactive, toRefs } from "vue";
import _ from "lodash";
export default {
  name: "WatcherComponent",
  setup() {
    const state = reactive({
      fname: "",
      lname: "",
      options: {
        heroName: "",
      },
    });

    // watch(() => {
    //     return {...state}
    // }, function (newVal, oldVal) {
    //     console.log('fname old value: ',  oldVal.fname)
    //     console.log('fname new value: ',  newVal.fname)
    //     console.log('lname old value: ',  oldVal.lname)
    //     console.log('lname new value: ',  newVal.lname)
    // })

    // watch(() => state.fname, function (newVal, oldVal) {
    //     console.log('fname old value: ',  oldVal)
    //     console.log('fname new value: ',  newVal)
    // })

    watch(
      () => _.cloneDeep(state.options),
      function (newVal, oldVal) {
        console.log("fname old value: ", oldVal);
        console.log("fname new value: ", newVal);
      },
      {
          deep: true,
      }
    );

    const firstName = ref("");
    const lastName = ref("");

    watch(
      [firstName, lastName],
      (newValues, oldValues) => {
        console.log("firstname old value: " + oldValues[0]);
        console.log("firstname new value: " + newValues[0]);

        console.log("lastname old value: " + oldValues[1]);
        console.log("lastname new value: " + newValues[1]);
      },
      {
        immediate: true,
      }
    );

    return {
      firstName,
      lastName,
      ...toRefs(state),
    };
  },
  data() {
    return {
      name: "",
    };
  },
  watch: {
    name(newValue, oldValue) {
      console.log(newValue, oldValue);
    },
  },
};
</script>

<style lang="scss" scoped>
</style>