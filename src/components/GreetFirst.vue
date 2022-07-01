<template>
    <div>
        <h2>Hello {{ name }}, Movie name is: {{ movie }}</h2>
    </div>
    <button @click="$emit('enlarge-text')">Enlarge text</button>
</template>

<script>
    export default {
        name: 'GreetFirst',
        props: ['name','movie'],
        emits: ['enlarge-text'],
    }
</script>

<style scoped>

</style>