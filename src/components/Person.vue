<template>
  <div>
    <input type="text" v-model="firstName">
    <input type="text" v-model="lastName">
  </div>
  <PersonGreeting 
  :firstName="firstName" 
  :lastName="lastName" 
  @callHeroes="callHeroes"/>
</template>

<script>
import PersonGreeting from './PersonGreeting.vue'
import { ref } from 'vue'
  export default {
    name: 'Person',
    components:{
      PersonGreeting
    },
    setup(){
      const firstName = ref('')
      const lastName = ref('')

      function callHeroes(hero){
        alert(`full name ${hero.value}`)
      }
      
      return{
        firstName,
        lastName,
        callHeroes
      }

    }
  }
</script>

<style scoped>

</style>