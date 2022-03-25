<template>
  <header class="row d-flex justify-content-between align-items-center">
      <div class="col-6 px-5">
          ciao sono header
      </div>
      <div class="col-6 text-end px-5">
        <label for="genre"></label>
        <select name="genre" id="genre">genre
            <option  value="null">-----</option>
            <option  value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option @change="consoleFunction" value="jazz">Jazz</option>
            <option value="metal">Metal</option>    
        </select>          
        
      </div>
      
  </header>
</template>

<script>
    export default {
        name: 'HeaderDisc',
        methods: {
            consoleFunction() {
                console.log('ciao');
        },
    }
}
</script>

<style>
    header{
        background-color: grey;
        height: 50px;
    }
</style>