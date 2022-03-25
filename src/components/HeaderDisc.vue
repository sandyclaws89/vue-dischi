<template>
  <header class="row d-flex justify-content-between align-items-center">
      <div class="col-6 px-5">
          ciao sono header
      </div>
      <div class="col-6 text-end px-5">
        <label for="genre"></label>
        <select name="genre" id="genre">genre
            <option  value="null">-----</option>
            <option @change="FunctionRock" value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option @change="FunctionJazz" value="jazz">Jazz</option>
            <option value="metal">Metal</option>    
        </select>          
        
      </div>
      
  </header>
</template>

<script>
    export default {
        name: 'HeaderDisc',
        data(){
            return {
                rock: 'rock',
                pop: 'pop',
                jazz: 'jazz',
                metal: 'metal',

            }
        },
        props:{

        },
        methods: {
            // FunctionRock() {
                // console:() => console.log();
        // },
        // functionLog() {
        //     this.console.log()
        // }
    }
}
</script>

<style>
    header{
        background-color: grey;
        height: 50px;
    }
</style>