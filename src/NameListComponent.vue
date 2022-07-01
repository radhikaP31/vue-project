<template>
  <div>
   <name-list>
     <template v-slot:default="slotProps">
       {{ slotProps.fullname }} {{ slotProps.movie }}
     </template>
   </name-list>

   <name-list>
     <template v-slot:default="slotProps">
       {{ slotProps.movie }} - {{ slotProps.fullname }} 
     </template>
   </name-list>

   <name-list>
     <template v-slot:default="slotProps">
       {{ slotProps.fullname }}
     </template>
   </name-list>

  </div>
</template>

<script>
import NameList from './components/NameList.vue';
  export default {
    name: 'App',
    components: {
      NameList
    },
    data() {
      return{

      }
    }
  }
</script>

<style lang="scss" scoped>

</style>