<template>
  <div>
    <h3>this is lifecycleC component</h3>
  </div>
</template>

<script>
import {onBeforeMount, onMounted, onBeforeUpdate, onUpdated} from 'vue'
  export default {
    name:  'lifecycleC',
    setup(){

      onBeforeMount(() => {
        console.log('this is onBeforeMount()')
      })
      onMounted(() => {
        console.log('this is onMounted()')
      })
      onBeforeUpdate(() => {
        console.log('this is onbefore onBeforeUpdated()')
      })
      
      onUpdated(() => {
        console.log('this is on onUpdated()')
      })
    }
  }
</script>

<style scoped>

</style>