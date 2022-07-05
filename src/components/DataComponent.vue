<template>
    <h2> Options - {{ o_firstname }}</h2>
    <h2> Options - {{ o_firstname }} {{ o_lastname }} a.k.a {{ o_heroname }}</h2>

    <h2> Composition - {{ c_firstname }}</h2>
    <h2> Composition Greet - {{ greet }}</h2>

    <h2> Composition - {{ c_firstname }} {{ c_lastname }} a.k.a {{ c_heroname }}</h2>
    <h2> Composition GreetHero - {{ greethero }}</h2>

    <h2> Composition Reactive - {{ state.firstname }} {{ state.lastname }} a.k.a {{ state.heroname }}</h2>
    <h2> Composition Reactive GreetHero - {{ rectiveGreetHero }}</h2>
</template>

<script>
    import { ref, reactive } from 'vue'
    export default {
        name: 'DataComponent',
        setup() {
            const c_firstname = ref('Clerk')
            const c_lastname = ref('Kent')
            const c_heroname = ref('Superman')

            const greet =  `Hello ${c_firstname.value}`
            const greethero = `Hello ${c_firstname.value} ${c_lastname.value} a.k.a ${c_heroname.value}`

            const state = reactive({
                firstname: ref('Princess'),
                lastname: ref('Diana'),
                heroname: ref('Wonder Woman')
            })

            const rectiveGreetHero = `Hello ${state.firstname} ${state.lastname} a.k.a ${state. heroname}` 

            return {
                c_firstname,
                c_lastname,
                c_heroname,
                greet,
                greethero,
                state,
                rectiveGreetHero,
            }
        },
        data() {
            return {
                o_firstname: 'Petter',
                o_lastname: 'Parker', 
                o_heroname: 'Spiderman'
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>