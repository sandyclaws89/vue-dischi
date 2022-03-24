<template>
  <main class="row">
      <div>

      </div>
     
  </main>
</template>

<script>
import axios from 'axios';

export default {
    name:'MainDisc',
    data () {
        return {

        }
    },
    components: {
        created() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        }
    }

}
</script>

<style>
    main{
        height: calc(100vh - 50px);
       
        background-color: cadetblue ;
    }
</style>