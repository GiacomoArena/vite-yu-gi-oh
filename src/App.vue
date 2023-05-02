
<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import FilterBar from './components/FilterBar.vue';
import axios from "axios";  


export default {
  name: "App",
  components:{
    Header,
    Main,
    FilterBar
  },
  data(){
    return{

    }
  },
  methods:{
    getApi(){
      axios.get(store.apiUrl)
      .then(result => {
        
      })
    }
  },
}

</script>

<template>

  <Header />

  <Main />

</template>

<style lang="scss">

</style>