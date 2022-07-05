<template>
    <div>
        <button @click="incrementCount"> Count {{ count }} times</button>
    </div>
</template>

<script>
    import CounterMixin from "../mixins/counter";
    export default {
        name: 'ClickCounter',
        mixins: [CounterMixin],
    }
</script>

<style lang="scss" scoped>

</style>