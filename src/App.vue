<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/beerLogo.png">
    <beer msg="Glossary of Beer"/>
    <Listbeer msg="Choose your Own Beer"/>
    <listbeer info/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import beer from './components/Beer.vue';
import Listbeer from './components/ListBeer.vue';


export default Vue.extend({
  name: 'app',
  components: {
    beer,
    Listbeer,
    
  },
});
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
