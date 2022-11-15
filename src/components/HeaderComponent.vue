<template>
  <h1 class="ps-2 pt-2">Breaking Bad Api</h1>
  <div class="container">
    <div class="dropdown pt-4">
      <select id="search" v-model="searchs">
  <option value="">scegli</option>
  <option :value="value.nome" v-for="(value) in option"> {{value.url}} </option>
</select>
   <button @click="searchCh">clicca qui</button>

    </div>
  </div>
</template>

<script>
  export default {
    data(){
      return{
        option:[
          {
            nome:'Breaking Bad',
            url:'Breaking+Bad'
          },
          {
            nome:'Better Call Saul',
            url:'Better+Call+Saul'
          }
          
      ],
        searchs:''
  }
},
props:{
  search:String
},
methods:{
  searchCh(){
    this.$emit('filtro', this.searchs);
   
  }
}
  }

</script>

<style lang="scss" scoped>
h1{
  color: white;
}
</style>