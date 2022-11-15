<template>
  <div class="container bg-white mt-4 pt-5">
<div class="found pt-3 pb-3 ps-3">
  <strong>Found 62 characters</strong>
</div>
<div class="d-flex row  cc">
  <div class="ab-col-5 pt-3"  v-for='(item,index) in  Charachter'>
    <div class="pb-3">
      <img :src="item.img" alt="">
    </div>
    <p><strong>{{item.name}}</strong></p>
    <p>{{item.status}}</p>
    <p>{{item.category}}</p>
  </div>
</div>
  </div>
</template>

<script>
  export default {
    props:['Charachter']
  }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variablse.scss' as *;
  .found{
    background: $secondarycolor;
    width: 95%;
    margin: auto;
    color: white;
  }
  .cc{
    width: 95%;
   margin: auto;
  text-align: center;
  }
  .ab-col-5{
    width: calc((100% - 150px) / 5);
  background: $primarycolor;
  color: gray;
    margin: 10px  15px;
  }
  img{
   width: 90%;
  }
  strong{
    color: white;
  }
</style>