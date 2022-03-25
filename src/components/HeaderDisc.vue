<template>
  <header class="row d-flex justify-content-between align-items-center">
      <div class="col-6 px-5">
          ciao sono header
      </div>
      <div class="col-6 text-end px-5">
        <label for=""></label>
        <select name="genre" id="rock">genre
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>    
        </select>          
        
      </div>
      
  </header>
</template>

<script>
export default {
    name: 'HeaderDisc',
}
</script>

<style>
    header{
        background-color: grey;
        height: 50px;
    }
</style>