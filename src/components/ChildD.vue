<template>
    <div>
        <h2>This is ChildD Component: Option- {{userName}}</h2>
        <h2>This is ChildD Component: Compsition childUserName- {{childUserName}}</h2>
        <h2>This is ChildD Component: Compsition child Count- {{childCount}}</h2>
        <h2>This is ChildD Component: Compsition child Hero Name- {{firstName}} {{lastName}}</h2>
        <button @click="incrementCount">Child Increment</button>
       
    </div>
</template>

<script>
import { inject, toRefs } from 'vue'
    export default {
        name: 'ChildD',
        setup(){
            const childUserName = inject('c_userName', 'Default userName')
            const childCount = inject('cref_count', 0)
            const childHero = inject('cref_hero', {})
            const incrementCount = inject('incrementCount')
            return{
                childUserName,
                childCount,
                ...toRefs(childHero),
                 incrementCount 
                

            }
        },
       
        inject: ['userName']
        
    }
</script>

<style scoped>

</style>