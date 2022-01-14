<template>
  <div>
    <h3>This is lifecycleO component</h3>
  </div>
</template>

<script>
  export default {
    name: 'lifecycleO',
    beforeCreate() {
      console.log('this is before created life cycle o()')
    },
    created(){
      console.log('this is  created life cycle o()')

    },
    beforeMount() {
      console.log('this is befroe mount life cycle o()')
      
    },
    mounted(){
      console.log('this is mounted life cycle o()')

    }
  }
</script>

<style scoped>

</style>
