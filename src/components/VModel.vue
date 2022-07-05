<template>
    <div>
        <input type="text" name="fname" id="fname" placeholder="F Name" v-model="fname"/>
        <input type="text" name="lname" id="lname" placeholder="L Name" v-model="lname"/>
        <br><br>
        <input type="text" name="heroName" id="heroName" placeholder="Hero Name" v-model="heroName"/>
        <input type="text" name="firstname" id="firstname" placeholder="First Name" v-model="firstname"/>
        <input type="text" name="lastname" id="lastname" placeholder="Last Name" v-model="lastname"/>
    </div>
</template>

<script>
import { ref, reactive, toRefs } from 'vue'
    export default {
        name: 'vModel',
        setup() {
            const heroName = ref('')
            const state = reactive({
                firstname: '',
                lastname: ''
            })

            return {
                heroName,
                ...toRefs(state),
            }
        },
        data () {
            return{
                fname: '',
                lname: '',
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>