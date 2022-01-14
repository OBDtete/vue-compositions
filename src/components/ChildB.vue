<template>
    <div>
        <h2>This is ChildB Component</h2>
        <ChildD />
    </div>
</template>

<script>
import ChildD from './ChildD.vue'
    export default {
        name: 'ChildB',
        components: {
            ChildD
        }
    }
</script>


<style scoped>

</style>