<template>
    <div>
        <h2> {{ name }}</h2>
    </div>
</template>

<script>
    import { ref } from 'vue'
    export default {
        name: 'DemoOneComponent',
        setup() {
            const name = ref('Demo One')

            setTimeout(() => {
                name.value = 'Demo Two'
                console.log(name)
            }, 2000);

            return {
                name
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>