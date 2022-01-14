<template>
  <div>
    <h3 @mouseover="increament">Clicked {{count}} times</h3>
  </div>
</template>

<script>
import useCounter  from '../composables/useCounter'
// import CounterMixin from '../mixins/counter'
  export default {
    name: 'HoverCounter',
    setup(){

      
      const {count, increament } = useCounter()

      return{
        count,
        increament
      }
    }
    // mixins:[CounterMixin]
  }
</script>

<style scoped>

</style>