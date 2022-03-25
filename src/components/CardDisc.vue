<template>
  <div class="card d-flex justify-content-center align-items-center">
        <img :src="DiscImg" :alt="DiscAuthor">
        <h2>{{DiscAuthor}}</h2>
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
      width: 80%;
      margin: 5px;
      flex-grow: 1;  
    };
    .card{
      padding: 5px;
      background-color: teal;
    }
 
</style>