<template>
  <div>
    <HeaderDisc/>
    <MainDisc/>
  </div>
</template>

<script>
import HeaderDisc from './components/HeaderDisc.vue';
import MainDisc from './components/MainDisc.vue';


export default {
  name: 'App',
  components: {
    HeaderDisc,
    MainDisc,
  }
}
</script>

<style lang= "scss">
    @import "~bootstrap/scss/bootstrap";
    @import "./assets/styles/style.scss";

</style>
