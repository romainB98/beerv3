<template>
  <div class="Listbeer">
    <h4>{{ info }}</h4>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import axios from 'axios';

export default Vue.extend({
  name: 'Listbeer',
  props: {
    msg: String,
  },
});

 new Vue({  
   el:'listBeer',
  data () {
    return {
      info: null
    }
  },
  mounted () {
    axios
      .get('https://sandbox-api.brewerydb.com/v2/beers/?key=3e3c1e4b6f4eaa862efa14b8a1009582')
      .then(response => (this.info = response.data.beers))
      
  }
})


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
