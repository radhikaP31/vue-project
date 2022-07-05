<template>
    <div>
        <button @click="incrementCount"> Count {{ count }} times</button>
    </div>
</template>

<script>
    import useCounter from "../composables/useCounter"
    export default {
        name: 'ClickCounterComponent',
        setup() {
            const { count, incrementCount} = useCounter(100, 10)

            return {
                count,
                incrementCount
            }
        }
    }
</script> 

<style lang="scss" scoped>

</style>