<template>
  <HeaderComponent/>
 <main>
  
 </main>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import NavBar from './components/NavBar.vue'
import CardsComponent from './components/CardsComponent.vue'
  export default {
    data(){
      return{
        apiURL:"https://www.breakingbadapi.com/api/characters"
      }
    },
    components:{
      HeaderComponent,
      NavBar,
      CardsComponent
    }
  }
</script>

<style lang="scss" scoped>

</style>