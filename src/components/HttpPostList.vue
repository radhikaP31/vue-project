<template>
    <div>
        <!-- <button @click="getPosts">Http Post List</button> uncomment if you need to load data on button click -->
        <h3 v-if="errorMsg"> {{ errorMsg }}</h3>
        <div v-for="post in posts" :key="post.id">
            <h3>{{ post.id }} {{ post.title }}</h3>
            <p> {{ post.body }}</p>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
    export default {
        name: 'HttpPostList',
        created() { //use for load data on page load
            this.getPosts()
        },
        data() {
            return {
                posts: [],
                errorMsg: '',
            }
        },
        methods: {
            getPosts(){
                axios.get('https://jsonplaceholder.typicode.com/posts')
                .then((response) => {
                    console.log(response.data)
                    this.posts = response.data
                })
                .catch((error) => {
                    console.log(error)
                    this.errorMsg = 'Error retriving data'
                })
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>