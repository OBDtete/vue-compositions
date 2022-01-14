<template>
    <div>
        <h2>This is ChildA Component</h2>
        <ChildB />
    </div>
</template>

<script>
import ChildB from './ChildB.vue'
    export default {
        name: 'ChildO',
        components: {
            ChildB
        }
    }
</script>

<style scoped>

</style>