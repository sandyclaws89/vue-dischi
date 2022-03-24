<template>
  <main>
      <div class="container">
           <CardDisc
           v-for:
           />
      </div>
     
     
  </main>
</template>

<script>
import axios from 'axios';
import CardDisc from './CardDisc.vue'

export default {
    name:'MainDisc',
    data () {
        return {

        }
    },
    components: {
      CardDisc,
    },
    created() {
        /*questa mi serve farla in asincrono perchè ci sono API che ci mettono tanto tempo.*/
        const promise= axios.get('https://flynn.boolean.careers/exercises/api/array/music');
        /*per renderla asincrona uso il .then, che è un metodo dell'oggetto che ritorna da .then */
        promise.then(function(NetworkResult) {
            
            console.log(NetworkResult.data);
            return NetworkResult.data;
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