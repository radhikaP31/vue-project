<template>
    <div>
        <input type="text" ref="inputRef"> 
    </div>
</template>

<script>
    export default {
        name: 'TemplateRef',
        components: {
        },
        mounted() {
            console.log(this.$refs.inputRef)
            this.$refs.inputRef.focus()
        },
    }
</script>

<style  scoped>

</style>