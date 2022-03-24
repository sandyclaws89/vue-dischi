<template>
  <main>
      <div class="container">
           <CardDisc
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
            arrDisc: [],
        };
    },
    components: {
      CardDisc,
    },
    created() {
        /*questa mi serve farla in asincrono perchè ci sono API che ci mettono tanto tempo.*/
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        /*per renderla asincrona uso il .then, che è un metodo dell'oggetto che ritorna da .then */
        .then(function(NetworkResult) {
            
            // console.log(NetworkResult.data.response);
            this.arrDisc = NetworkResult.data.response;
            console.log(this.arrDisc);
        })
    }
};
</script>

<style>
    main{
        height: calc(100vh - 50px);
       
        background-color: cadetblue ;
    }
</style>