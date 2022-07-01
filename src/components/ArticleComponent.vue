<template>
    <div>
        <div>
            <h2>Article Component</h2>
        </div>
        <h2 v-bind="$attrs"> Title: {{ title }}</h2>  <!-- id attribute added to this tag -->
        <h2> Likes: {{ likes }}</h2>
        <h2> Published: {{ isPublished ? 'Yes' : "No" }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'ArticleComponent',
        props: {
            title: {
                type: String,
                required: true,
                default: 'Batman',
            },
            likes: Number,
            isPublished: Boolean,
           
        },
        inheritAttrs: false
    }
</script>

<style scoped>

</style>