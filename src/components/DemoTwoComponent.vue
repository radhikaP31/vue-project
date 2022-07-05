<template>
    <div>
        <h2> {{ firstname }} {{ lastname }}</h2>
        <h2> {{ fname }} {{ lname }}</h2>
    </div>
</template>

<script>
    import { reactive, toRefs } from 'vue'
    export default {
        name: 'DemoTwoComponent',
        setup() {
            const state = reactive({
               firstname: 'Bruce',
               lastname: 'Wayne',
            })

            setTimeout(() => {
                state.firstname = 'Clark'
                state.lastname = 'Lee'
                console.log(state)
            }, 2000);

            return toRefs(state)
        },
        data() {
            return {
                fname: 'Peter',
                lname: 'Parker',
            }
        }

    }
</script>

<style lang="scss" scoped>

</style>