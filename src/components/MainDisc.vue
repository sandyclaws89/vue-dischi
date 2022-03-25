<template>
  <main>
      <div>
          <div class="mine-container  d-flex justify-content-center">
           <CardDisc v-for="(disc, index) in arrDisc" :key="index"
           :disc-img="disc.poster"
           :disc-title="disc.title"
           :disc-author="disc.author"
           :disc-genre="disc.genre"
           :disc-year="disc.year"
           class="card-main"
           />
            </div>
            <div class="mine-container  d-flex justify-content-center">
           <CardDisc v-for="(disc, index) in arrDisc" :key="index"
           :disc-img="disc.poster"
           :disc-title="disc.title"
           :disc-author="disc.author"
           :disc-genre="disc.genre"
           :disc-year="disc.year"
           class="card-main"
           />
            </div>
<!--         
           <CardDiscRock v-for="(disc, index) in arrDisc.index.genre" :key="index"
           :disc-img="disc.poster"
           :disc-title="disc.title"
           :disc-author="disc.author"
           :disc-genre="disc.genre"
           :disc-year="disc.year"
           class="card-main"
           /> -->
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

<style lang="scss">
    main{
        background-color: cadetblue ;
        padding-bottom: 100px;
        padding-top: 20px;
    }
    .card-main{
        width: calc((100% - 250px) / 5);
        margin: 5px;
    };
    .mine-container{
        flex-wrap: wrap;
    };
</style>