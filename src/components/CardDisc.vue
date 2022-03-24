<template>
  <div class="row d-flex justify-content-center">
      <div class="offset-2 col-2">
        <img :src="DiscImg" :alt="DiscAuthor">
        <h1>{{DiscAuthor}}</h1>
        <div class="title">{{DiscGenre}}</div>
        <span>{{DiscYear}}</span>
      </div>
  </div>
</template>

<script>
export default {
    name:'CardDisc',
    props:{
        DiscImg: String,
        DiscTitle: String,
        DiscAuthor: String,
        DiscGenre: String,
        DiscYear: String,
    }
}
</script>

<style scoped lang="scss" >
   
    img{
      width: 100px;
      margin: 5px;  
    }
    .title{
        display: block;
    }
</style>