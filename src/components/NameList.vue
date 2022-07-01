<template>
    <h3 v-for="name in names" :key="name.fullname">
         <slot :fullname="name.fullname" :movie="name.movie"></slot>
    </h3>
</template>

<script>
    export default {
        name: 'NameList',
        data() {
            return {
                names:[
                    {
                    'fullname': 'Christian Bale',
                    'movie': 'The Prestige',
                    },
                    {
                    'fullname': 'Di Caprio',
                    'movie': 'Inception',
                    },
                    {
                    'fullname': 'Robert Drowny Junior',
                    'movie': 'Ironman',
                    },
                    
                ],
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>