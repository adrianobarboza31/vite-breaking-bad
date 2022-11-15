<template>
  <HeaderComponent @filtro="getCharachters"/>
 <main>
  <CardsComponent :Charachter="charachterList"/>
 </main>
</template>

<script>
import axios from 'axios';
import HeaderComponent from './components/HeaderComponent.vue'
import NavBar from './components/NavBar.vue'
import CardsComponent from './components/CardsComponent.vue'
  export default {
    data(){
      return{
        apiURL:"https://www.breakingbadapi.com/api/characters",
        charachterList:[],
        search:''
      }
    },
    components:{
      HeaderComponent,
      NavBar,
      CardsComponent
    },
    methods:{
      getCharachters(value){
        console.log(value)
        const api=(value)?this.apiURL+'?category='+value:this.apiURL;
        axios.get(api).then(
          (res)=>{
            this.charachterList=[...res.data];
            console.log(this.charachterList)
          },
          )
         
      },

    },
    created(){
      this.getCharachters()
    }
    // characters?category=Better+Call+Saul
    // "char_id":1,"name":"Walter White","birthday":"09-07-1958","occupation":["High School Chemistry Teacher","Meth King Pin"],"img":"https://images.amcnetworks.com/amc.com/wp-content/uploads/2015/04/cast_bb_700x1000_walter-white-lg.jpg","status":"Presumed dead","nickname":"Heisenberg","appearance":[1,2,3,4,5],"portrayed":"Bryan Cranston","category":"Breaking Bad","better_call_saul_appearance":[]}
  }
</script>

<style lang="scss" scoped>

</style>