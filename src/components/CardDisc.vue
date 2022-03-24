<template>
  <div>
        <img :src="DiscImg" :alt="DiscAuthor">
        <h1>{{DiscAuthor}}</h1>
        <div>{{DiscGenre}}</div>
        <span>{{DiscYear}}</span>
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
    // div{
    //     width: calc((100% - 5px)/5)
    // }
</style>