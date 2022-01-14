<template>
  <div>
    <button @click="increament">Clicked {{count}} times</button>
  </div>
</template>

<script>
import useCounter from '../composables/useCounter'
// /import CounterMixin from '../mixins/counter'
  export default {
    name: 'ClickCounter',
    setup(){
      const {count, increament } = useCounter(100, 10)

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