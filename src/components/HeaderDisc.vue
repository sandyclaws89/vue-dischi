<template>
  <header class="row d-flex justify-content-between align-items-center">
      <div class="col-6 px-5">
          ciao sono header
      </div>
      <div class="col-6 text-end px-5">
        <label for="genre"></label>
        <select @change="rockFunction" name="genre" id="genre">genre
            <option value="null">-----</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>    
        </select>          
        
      </div>
      <!-- PSEUDOCODIFICA PER FILTRARE PER GENERE -->
      <!--  
            METTO UN EVENTO CHANGE AD OGNI OPTION
            CON LE PROPS PORTO I DATI NEL MAIN
            CREO UN   -->
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
            rockFunction(test) {
            console.log(test)
  }
    }
}
</script>

<style>
    header{
        background-color: grey;
        height: 50px;
    }
</style>