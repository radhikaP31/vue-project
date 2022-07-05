<template>
    <div>
        <input type="text" name="fname" id="fname" placeholder="F Name" v-model="fname"/>
        <input type="text" name="lname" id="lname" placeholder="L Name" v-model="lname"/>
        <h2> Option fullname is {{ fullName }}</h2>

        <input type="text" name="fname" id="fname" placeholder="F Name" v-model="refFname"/>
        <input type="text" name="lname" id="lname" placeholder="L Name" v-model="refLname"/>
        <h2> Ref fullname is {{ refFullname }}</h2>

        <input type="text" name="fname" id="fname" placeholder="F Name" v-model="reactiveFname"/>
        <input type="text" name="lname" id="lname" placeholder="L Name" v-model="reactiveLname"/>
        <h2> Reactive fullname is {{ reactiveFullname }}</h2>

    </div>
</template>

<script>
import { ref, computed, reactive, toRefs } from "vue";
    export default {
        name: 'ComputedComponent',
        setup() {
            const refFname = ref('')
            const refLname = ref('')

            const refFullname = computed(function() {
                return `${refFname.value} ${refLname.value}`
            })

            const state = reactive({
                reactiveFname: '',
                reactiveLname: ''
            })

            const reactiveFullname = computed(function() {
                return `${state.reactiveFname} ${state.reactiveLname}`
            })

            return {
                refFname,
                refLname,
                refFullname,
                ...toRefs(state),
                reactiveFullname
            }
        },
        data () {
            return{
                fname: '',
                lname: '',
            }
        },
        computed: {
            fullName() {
                return `${this.fname} ${this.lname}`
            }
        }

    }
</script>

<style lang="scss" scoped>

</style>