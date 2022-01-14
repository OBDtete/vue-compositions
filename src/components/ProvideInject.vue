<template>
    <div>
        <h2>This is Parent Component: Count {{count}}</h2>
        <h2>This is Parent Component: Option name {{name}}</h2>
        <h2>This is Parent Component: Hreo {{firstName}} {{lastName}}</h2>
        <button @click="incrementCount">Increment count</button>
        <ChildO />
    </div>
</template>

<script>
import { provide, ref, reactive, toRefs } from 'vue'
import ChildO from './ChildO.vue'
    export default {
        name: 'ProvideInject',

        components:{
            ChildO
        },
        setup(){
            provide('c_userName', 'OBDC')

            const count = ref(0)
             function incrementCount() {
                count.value++
            }
            const state = reactive({
                firstName: 'Bruce',
                lastName: 'Wayne'                
            })
            provide('cref_count', count)
            provide('cref_hero', state)
            provide('incrementCount', incrementCount )
            return{
                count,
                ...toRefs(state),
                incrementCount 
            }
        },
       data(){
            return{
                name: 'OBD'

            }

        },
        provide(){
            return{
                userName: this.name
            }
        }
       
    }
</script>

<style scoped>

</style>