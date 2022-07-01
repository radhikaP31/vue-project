<template>
  <h2>Component F</h2>
  <h3>Component F App Name display with inject - {{ appname }}</h3>
</template>

<script>
export default {
  name: 'ComponentF',
  inject: ['appname'],
}
</script>

<style scoped>
</style>