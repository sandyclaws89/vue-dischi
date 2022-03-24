<template>
  <main>
      <div class="mine-container flex">
           <CardDisc v-for="(disc, index) in arrDisc" :key="index"
           :disc-img="disc.poster"
           :disc-title="disc.title"
           :disc-author="disc.author"
           :disc-genre="disc.genre"
           :disc-year="disc.year"
           class="card"
           />
      </div>
     
     
  </main>
</template>

<script>
import axios from 'axios';
import CardDisc from './CardDisc.vue';

export default {
    name:'MainDisc',
    data () {
        return {
            arrDisc: null,
        };
    },
    components: {
      CardDisc,
    },
    created() {
        /*questa mi serve farla in asincrono perchè ci sono API che ci mettono tanto tempo.*/
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        /*per renderla asincrona uso il .then, che è un metodo dell'oggetto che ritorna da .then */
        .then((NetworkResult)=> {
            // console.log(NetworkResult.data.response);
            this.arrDisc = NetworkResult.data.response;
            console.log(this.arrDisc);
        });
    },
};
</script>

<style>
    main{
        height: calc(100vh - 50px);
        background-color: cadetblue ;
    }
    .card{
        width: calc((100% - 2.5px)/5);
    };
    .mine-container{
        flex-wrap: nowrap;
    }
</style>